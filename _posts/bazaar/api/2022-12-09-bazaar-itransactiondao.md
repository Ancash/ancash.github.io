---
title: "Bazaar API: ITransactionDAO"
date: 2022-12-09 14:00:00 +0100
categories: [Minecraft, Bazaar]
tags: [bazaar, api, dao]     # TAG names should always be lowercase
---

In order to get the [ITransactionDAO](/doc/bazaar/de/ancash/bazaar/core/dao/ITransactionDAO.html), you have to execute
```java
ITransactionDAO transactionDAO = coreDAO.transactionsDAO();
```

This DAO makes it possible to create Sell Offers, create Buy Orders and check whether a player is able to create an enquiry.
Here is the method to create a Sell Offer/Buy Order
```java
public boolean createBuyOrder(UUID uuid, int amount, double unitPrice, int cat, int sub, int subsub) {...}

public boolean createSellOffer(UUID uuid, int amount, double unitPrice, int cat, int sub, int subsub) {...}
```
As you can see, their parameters are identical. The first is the UUID of the player you want to create an enquiry for, the second and third are self explaining. The last three integers are the [Main Category]({{site.baseurl}}/posts/bazaar-category), the [Sub Category]({{site.baseurl}}/posts/bazaar-sub-category) and the [Sub Sub Category]({{site.baseurl}}/posts/bazaar-sub-sub-category) the enquiry should be created in. *true* is returned on success, *false* otherwise. All of the methods do not take the players money balance into consideration, so a seperate check is needed.

This method checks if the specified player can create an enquiry/does not exceed the limit
```java
public boolean canCreateEnquiry(UUID uuid) {...}
```

As you may have noticed there are a few other methods available. These are used internally to handle specific, more complex events (specified by the method name). As such it's not recommended to use these methods, there's a lot happening outside those methods to make things work, and no documentation will be provided. However if you need some of the undocumented methods, a small documentation can be provided.