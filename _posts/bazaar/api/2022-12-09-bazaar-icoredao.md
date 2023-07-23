---
title: "Bazaar API: ICoreDAO"
date: 2022-12-09 13:00:00 +0100
categories: [Minecraft, Bazaar]
tags: [bazaar, api, dao]     # TAG names should always be lowercase
---

As the name suggests, this is the main part of the Bazaar API. Here is a list of methods with a short explanation:

```java
public ITransactionDAO transactionDAO();
```
See [ITransactionDAO]({{site.baseurl}}/posts/bazaar-itransactiondao)
```java
public IStatisticsDAO statisticsDAO();
```
See [IStatisticsDAO]({{site.baseurl}}/posts/bazaar-istatisticsdao)
```java
public IPlaceholderDAO placeholderDAO();
```
See [IPlaceholderDAO]({{site.baseurl}}/posts/bazaar-iplaceholderdao)
```java
public HashMap<String, Number> getHighestEnquiry(EnquiryType type, int cat, int sub, int subsub);
```
This method returns the enquiry (EnquiryType is either SELL_OFFER or BUY_ORDER) with the highest unit price in the specified [Main]({{site.baseurl}}/posts/bazaar-category), [Sub]({{site.baseurl}}/posts/bazaar-sub-category) and [Sub Sub]({{site.baseurl}}/posts/bazaar-sub-sub-category) category. May be null. If there are multiple enquiries with the highest unit price, which one is chosen is undefined.

```java
public HashMap<String, Number> getLowestEnquiry(EnquiryType type, int cat, int sub, int subsub);
```
This method returns the enquiry (EnquiryType is either SELL_OFFER or BUY_ORDER) with the lowest unit price in the specified [Main]({{site.baseurl}}/posts/bazaar-category), [Sub]({{site.baseurl}}/posts/bazaar-sub-category) and [Sub Sub]({{site.baseurl}}/posts/bazaar-sub-sub-category) category. May be null. If there are multiple enquiries with the lowest unit price, which one is chosen is undefined.

```java
public HashMap<Long, HashMap<String, Number>> getHighestEnquiries(EnquiryType type, int cat, int sub, int subsub);
```
This method returns the enquiries (EnquiryType is either SELL_OFFER or BUY_ORDER) with the highest unit price in the specified [Main]({{site.baseurl}}/posts/bazaar-category), [Sub]({{site.baseurl}}/posts/bazaar-sub-category) and [Sub Sub]({{site.baseurl}}/posts/bazaar-sub-sub-category) category. May be null. If there are multiple enquiries with the highest unit price, all will be returned.


```java
public HashMap<Long, HashMap<String, Number>> getLowestEnquiries(EnquiryType type, int cat, int sub, int subsub);
```
This method returns the enquiries (EnquiryType is either SELL_OFFER or BUY_ORDER) with the lowest unit price in the specified [Main]({{site.baseurl}}/posts/bazaar-category), [Sub]({{site.baseurl}}/posts/bazaar-sub-category) and [Sub Sub]({{site.baseurl}}/posts/bazaar-sub-sub-category) category. May be null. If there are multiple enquiries with the lowest unit price, all will be returned.


```java
public double getHighestEnquiryPrice(EnquiryType type, int cat, int sub, int subsub);
```
Returns the highest unit price of the specified EnquiryType in the specified [Main]({{site.baseurl}}/posts/bazaar-category), [Sub]({{site.baseurl}}/posts/bazaar-sub-category) and [Sub Sub]({{site.baseurl}}/posts/bazaar-sub-sub-category) category. If there is none, a value <= 0d will be returned.


```java
public double getHighestEnquiryPriceOrDefault(EnquiryType type, int cat, int sub, int subsub);
```
Returns the highest unit price of the specified EnquiryType in the specified [Main]({{site.baseurl}}/posts/bazaar-category), [Sub]({{site.baseurl}}/posts/bazaar-sub-category) and [Sub Sub]({{site.baseurl}}/posts/bazaar-sub-sub-category) category. If there is none, a default value defined in the [config.yml]({{site.baseurl}}/posts/bazaar-config) will be returned.


```java
public double getLowestEnquiryPrice(EnquiryType type, int cat, int sub, int subsub);
```
Returns the lowest unit price of the specified EnquiryType in the specified [Main]({{site.baseurl}}/posts/bazaar-category), [Sub]({{site.baseurl}}/posts/bazaar-sub-category) and [Sub Sub]({{site.baseurl}}/posts/bazaar-sub-sub-category) category. If there is none, a value <= 0d will be returned.


```java
public double getLowestEnquiryPriceOrDefault(EnquiryType type, int cat, int sub, int subsub);
```
Returns the lowest unit price of the specified EnquiryType in the specified [Main]({{site.baseurl}}/posts/bazaar-category), [Sub]({{site.baseurl}}/posts/bazaar-sub-category) and [Sub Sub]({{site.baseurl}}/posts/bazaar-sub-sub-category) category. If there is none, a default value defined in the [config.yml]({{site.baseurl}}/posts/bazaar-config) will be returned.


```java
public Triplet<Double, Integer, Integer> getKthLargestEnquiry(EnquiryType type, int cat, int sub, int subsub, int k);
```


```java
public Triplet<Double, Integer, Integer> getKthSmallestEnquiry(EnquiryType type, int cat, int sub, int subsub, int k);
```


```java
public HashMap<String, Number> getEnquiryAsMap(UUID uuid, long id, EnquiryType type);
```
Get a specific enquiry of a player. The enquiry id has to be provided.


```java
public HashMap<Long, HashMap<String, Number>> getEnquiriesAsMap(UUID uuid, EnquiryType type);
```
Get all enquiries with the specified type of a specific player.


```java
public int sumEnquiries(EnquiryType type, int cat, int sub, int subsub);
```
Returns the sum of the content of all Enquiries in the specified category. If subsub <= 0, the sum of all Enquiries in the sub category will be returned. It's recommended to use the lazy version of this method (see below) due to performance issues.


```java
public int countEnquiries(EnquiryType type, int cat, int sub, int subsub);
```
Returns the sum of all Enquiries in the specified category. If subsub <= 0, the count of all Enquiries in the sub category will be returned. It's recommended to use the lazy version of this method (see below) due to performance issues.


```java
public int lazySumEnquiries(EnquiryType type, int cat, int sub, int subsub);
```
Returns the sum of the content of all Enquiries in the specified category. If subsub <= 0, the sum of all Enquiries in the sub category will be returned. This lazy method does not actually sum all the enquiries, instead the value of a counter, that increments and decrements as needed, will be returned.


```java
public int lazyCountEnquiries(EnquiryType type, int cat, int sub, int subsub);
```
Returns the sum of all Enquiries in the specified category. If subsub <= 0, the count of all Enquiries in the sub category will be returned. This lazy method does not actually count all the enquiries, instead the value of a counter, that increments and decrements as needed, will be returned.


```java
public int countEnquiries(UUID uuid);
```
Returns the numbe of Enquiries owned by player.


```java
public boolean existEnquiries(EnquiryType type, int cat, int sub, int subsub);
```
Returns true if Enquiries with the specified type exist in the specified category.


```java
public double getClaimableCoins(UUID uuid);
```
Returns a players' claimable coins.


```java
public int getClaimableItems(UUID uuid);
```
Returns a players' claimable items. Note that one item is not always equal one item in game, it is possible to define an item in the bazaar as two or more in game items.


```java
public int getClaimable(UUID uuid, long id, EnquiryType type);
```
Returns the number of claimable coins or items.


```java
public int getLeft(UUID uuid, long id, EnquiryType type);
```
Returns how many items are left in the specified enquiry.


```java
public int getTax();
```
Returns tax in %.


```java
public double getRemnants(UUID id);
```
Returns a players' unused coins (read [here]({{site.baseurl}}/posts/bazaar-buy-order) for explanation).


```java
public double getRemnants(UUID uuid, long id);
```
Returns the remnants of the specific BuyOrder (read [here]({{site.baseurl}}/posts/bazaar-buy-order) for explanation). 