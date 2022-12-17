---
title: "Bazaar Command: set"
date: 2022-12-10 11:00:00 +0100
categories: [Minecraft, Bazaar]
tags: [bazaar, command]     # TAG names should always be lowercase
---

# Bazaar Command: set

This command allows you to set some items that are displayed in the Bazaar. For the changes to take effect [*/bz reload*]({{site.baseurl}}/posts/bazaar-cmd-reload) has to be executed.
The permission is: *bazaar.set*
## original
***/bz set original <1-5> <1-18> <1-9>*** takes an additional three numbers as arguments. These numbers are the [Category]({{site.baseurl}}/posts/bazaar-category), [Sub Category]({{site.baseurl}}/posts/bazaar-sub-category) and [Sub Sub Category]({{site.baseurl}}/posts/bazaar-sub-sub-category) the item you are holding will be set in. The *original* item is the item that will be used for transactions.

## sss
***/bz set sss <1-5> <1-18> <1-9>*** takes an additional three numbers as arguments. These numbers are the [Category]({{site.baseurl}}/posts/bazaar-category), [Sub Category]({{site.baseurl}}/posts/bazaar-sub-category) and [Sub Sub Category]({{site.baseurl}}/posts/bazaar-sub-sub-category) the item you are holding will be set in. This item represents a [Sub Sub Category]({{site.baseurl}}/posts/bazaar-sub-sub-category). This means that it'll be displayed in the specified Sub Category and can hold placeholders. Here are the placeholders that can be used:
* %offers_price_lowest% *//the lowest [Sell Offer]({{site.baseurl}}/posts/bazaar-sell-offer) unit price*
* %offers_price_highest% *//the highest Sell Offer unit price*
* %orders_price_lowest% *//the lowest [Buy Order]({{site.baseurl}}/posts/bazaar-buy-order) unit price*
* %orders_price_highest% *//the highest Buy Order unit price*
* %offers_price_lowest_stack% *//stack price of the Sell Offer with the lowest unit price*
* %offers_price_highest_stack% *//stack price of the Sell Offer with the highest unit price*
* %orders_price_lowest_stack% *//stack price of the Buy Order with the lowest unit price*
* %orders_price_highest_stack% *//stack price of the Buy Order with the highest unit price*
* %offers_total%& *//the amount of Sell Offers*
* %orders_total%& *//the amount of Buy Orders*
* %offers_content%& *//the amount of Sell Offers*
* %offers_content%& *//the amount of items in all Sell Offers*
* %orders_content%& *//the amount of items in all Buy Orders*

## s
***/bz set s <1-5> <1-18>*** takes an additional two numbers as arguments. These numbers are the [Category]({{site.baseurl}}/posts/bazaar-category) and [Sub Category]({{site.baseurl}}/posts/bazaar-sub-category) the item you are holding will be set in. This item represents a [Sub Category]({{site.baseurl}}/posts/bazaar-sub-category). This means that it'll be displayed in the specified Category and can hold placeholders. Here are the placeholders that can be used:
* %offers_price_lowest% *//the lowest [Sell Offer]({{site.baseurl}}/posts/bazaar-sell-offer) unit price*
* %offers_price_highest% *//the highest Sell Offer unit price*
* %orders_price_lowest% *//the lowest [Buy Order]({{site.baseurl}}/posts/bazaar-buy-order) unit price*
* %orders_price_highest% *//the highest Buy Order unit price*
* %offers_price_lowest_stack% *//stack price of the Sell Offer with the lowest unit price*
* %offers_price_highest_stack% *//stack price of the Sell Offer with the highest unit price*
* %orders_price_lowest_stack% *//stack price of the Buy Order with the lowest unit price*
* %orders_price_highest_stack% *//stack price of the Buy Order with the highest unit price*
* %offers_total%& *//the amount of Sell Offers*
* %orders_total%& *//the amount of Buy Orders*
* %offers_content%& *//the amount of Sell Offers*
* %offers_content%& *//the amount of items in all Sell Offers*
* %orders_content%& *//the amount of items in all Buy Orders*