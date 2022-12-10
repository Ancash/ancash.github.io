---
title: "Bazaar API: IStatisticsDAO"
date: 2022-12-09 15:00:00 +0100
categories: [Minecraft, Bazaar]
tags: [bazaar, api, dao]     # TAG names should always be lowercase
---

# Bazaar API: IStatisticsDAO

In order to get the [IStatisticsDAO](/doc/bazaar/de/ancash/bazaar/core/dao/IStatisticsDAO.html), you have to execute
```java
IStatisticsDAO statisticsDAO = coreDAO.statisticsDAO();
```

These types of transactions are being recorded:
* [Buy Instantly](/doc/bazaar/de/ancash/bazaar/core/record/Record.RecordDataType.html#BUY_INSTANTLY)
* [Sell Instantly](/doc/bazaar/de/ancash/bazaar/core/record/Record.RecordDataType.html#SELL_INSTANTLY)
* [Sell Offer](/doc/bazaar/de/ancash/bazaar/core/record/Record.RecordDataType.html#SELL_OFFER)
* [Buy Order](/doc/bazaar/de/ancash/bazaar/core/record/Record.RecordDataType.html#BUY_ORDER)

The unit price, the amount and the timestamp of a transaction are the only things that are being saved.

## Accessing records

To access the records of a specific year
```java
public Record getRecord(int year)
```

To access the records of a specific year and month
```java
public Record getRecord(int year, int month)
```

To access the records of a specific year, month and day
```java
public Record getRecord(int year, int month, int day)
```

To access the records of a specific year, month, day and hour. Offset should be set to true if the given date should take your time zone offset into consideration (UTC is desired).
```java
public Record getRecord(int year, int month, int day, int hour, boolean offset)
```

Although the methods above provide easy access to a record at a specific point in time, especially the third method, that does not take hours but days into consideration, does not consider time zone offsets. If the offset is, for example, +6 hours, the data of the current date is only returned, once it's 6 o'clock or late, thus not being very accurate. Although that also the case for the first and seconds methods, compared to the whole data set, it does not make that much of a difference, but it still does.

The following methods help in such a predicament.

Returns all the records that were made in the last n hours.
```java
public Record[] getRecordsOfLastHours(int n)
```

Returns all the records that were made in the last n days.
```java
public Record[] getRecordsOfLastDays(int n)
```

Returns all the records that were made in the last n months.
```java
public Record[] getRecordsOfLastMonths(int n)
```

Returns all the records that were made in the last n years.
```java
public Record[] getRecordsOfLastYears(int n)
```

The returned array is of the size n and an element, which may be null, in the array is the record that was saved it's index + 1 hours/days/months/years ago (compared to *System.currentTimeMillis()* (UTC)). Depending on how much data has been accumulated, it will take up a significant amount of memory. If sockets are not supported, that is not an issue, but if they are, performance issues will arise as the requested data grows bigger and bigger. Let's say a yearly record has been requested. It has 365 day * 24 hours * 100 transactions worth of data (876000). In it's serialized form, which is needed in order to send it over the network, it is ~80MB big, noticeably influencing performance. Therefore, in case of big data sets and performance issues, it's recommended to use the methods listed at the beginning.

## Manually saving records
It is possible to manually save a record by calling one of the two versions of [IStatisticsDAO#addRecord](/doc/bazaar/de/ancash/bazaar/core/dao/IStatisticsDAO.html#addRecord-de.ancash.bazaar.core.record.Record.RecordDataType-int-double-int:A-).
```java
//Version 1
statisticsDAO.addRecord(Record.RecordDataType type, int amount, double unitPrice, int[] category);
//Version 2
statisticsDAO.addRecord(Record.RecordDataType type, int amount, double unitPrice, int[] category, long millis, boolean offset);
```
Both version behave very similar. 
The first argument is one of the [RecordDataTypes](/doc/bazaar/de/ancash/bazaar/core/record/Record.RecordDataType.html) as listed at the beginning.
The second and third arguments are self explaining.
The fourth argument is an integer array with a length of 3. It contains the category the transaction took place. The first index is the [Main Category]({{site.baseurl}}/posts/bazaar-category), the second the [Sub Category]({{site.baseurl}}/posts/bazaar-sub-category) and the third the [Sub Sub Category]({{site.baseurl}}/posts/bazaar-sub-sub-category).

Version 2 differs by two arguments. It takes an additional long and boolean. The long is the difference, measured in milliseconds, between the current time and midnight, January 1, 1970 (your time zone, may or may not be UTC)), the boolean indicates whether the long takes the time zone into consideration or not. If it's set to true, the offset of your time zone is being added or subtracted (depending on the offset) from the long argument to match it's UTC equivalent.

As an example, Version 1 internally uses Version 2 as shown below, since *System.currentTimeMillis()* returns the difference, measured in milliseconds, between the current time and midnight, January 1, 1970 UTC.
```java
public boolean addRecord(Record.RecordDataType type, int amount, double unitPrice, int[] category) {
    addRecord(type, amount, unitPrice, category, System.currentTimeMillis(), false);
}

public boolean addRecord(Record.RecordDataType type, int amount, double unitPrice, int[] category, long millis, boolean offset) {
    ...
}
```