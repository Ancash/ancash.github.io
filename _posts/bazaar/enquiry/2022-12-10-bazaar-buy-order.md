---
title: "Bazaar: Buy Order"
date: 2022-12-10 14:00:00 +0100
categories: [Minecraft, Bazaar]
tags: [bazaar, enquiry]
---

A Buy Order signifies that a player is willing to buy a specific number of items at a specific price per unit or lower. \
Restrictions can be configure in the *plugins/Bazaar/config.yml* on the remote or by using [*/bz edit*]({{site.baseurl}}/posts/bazaar-cmd-edit) and selecting *config.yml*. \
Depending on the unit price, your Buy Order will be filled faster or slower (the higher the unit price, the faster it will be filled). \
There is one key difference between a [Sell Offer]({{site.baseurl}}/posts/bazaar-sell-offer) and a Buy Order. \
It is possibe for a Buy Order to be filled by a Sell Offer with an equal **OR** lower unit price. \
If the unit price is **NOT** the same, there are unused coins, called remnants. \
Only Buy Orders can have remnants. \
The formula for remnants is straighforward: *(BuyOrder#unitPrice - SellOffer#unitPrice) * amount*. 

## How to create a Buy Order
![Creating a Buy Order](/assets/bazaar/bz_create_buy.gif "Creating a Buy Order")

## How to fill a Buy Order
A Buy Order can either be filled by [instantly selling]({{site.baseurl}}/posts/bazaar-sell-instantly) the specific item at the specified unit price, or by a Sell Offer with a unit price equal or lower compared to the Buy Order:
![Filling a Sell Offer](/assets/bazaar/bz_fill_enquiry.gif "Filling a Sell Offer")

## Cancelling a Buy Order
See [here]({{site.baseurl}}/posts/bazaar-cancel-enquiry).