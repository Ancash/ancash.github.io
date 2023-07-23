---
title: "Bazaar: config.yml"
date: 2022-12-10 14:00:00 +0100
categories: [Minecraft, Bazaar]
tags: [bazaar, config]     # TAG names should always be lowercase
---

Here is a list of all options in *config.yml* and their default values
```yaml
socket:
   server-name: "Bazaar-01"
   enabled: false
   address: localhost
   port: 25000
tax: 4 #in %
bypass-bz-sub-cmds-list: false
no-permission: "§cYou don't have permission to do that!"
mustBeCreative: "§cMust be in creative mode to execute command!"

enquiry:
   rounding-places: 2
   max: 27
   unit-price:
      max: 1000000000
      min: 0.1

refund:
   sell-offer:
      refund-type: EDUCT
      factor: 1
      message: "§eRrefunded §a%refund% §eitems for one of your corrupted enquiries!"
   buy-order:
      refund-type: EDUCT
      factor: 1
      message: "§eRrefunded §a%refund% §ecoins for one of your corrupted enquiries!"

input:
   input-type: ANVIL
   chat:
      integer:
         invalid: "§6[Bazaar] §cInvalid integer"
         initial-message: "§6[Bazaar] §aEnter item amount"
      double: 
         invalid: "§6[Bazaar] §cInvalid decimal"
         initial-message: "§6[Bazaar] §aEnter price per unit"
   anvil:
      integer:
         invalid: "Invalid integer"
         title: "Enter item amount"
      double:
         invalid: "Invalid decimal"
         title: "Enter price per unit"

kthLargestBuyOrder: "§8- §6%unit_price% coins §7each §f: §a%sum%§7x from §f%count% orders"
kthSmallestSellOffer: "§8- §6%unit_price% coins §7each §f: §a%sum%§7x from §f%count% offers"

buyInstantly: "§6Bazaar! §7 Bought §a%amount%§7x §r%displayname% for §6%price% coins §7!"
sellInstantly: "§6Bazaar! §7 Sold  §a%amount%§7x §r%displayname% for §6%price% coins §7!"

claimedSellOffer: "§6Bazaar! §7Claimed §6%price% coins §7from selling §a%amount%§7x %displayname% §7at §6%unit_price% §7each!"
claimedBuyOrder: "§6Bazaar! §7Claimed §a%amount%§7x %displayname% §7worth §6%price% coins §7bought for §6%unit_price% §7each!"
collectedRemnants: "§6Bazaar! §7Collected §6%remnants% §7unused §6coins!"

noMoney: "§cYou don't have enough money!"
inventoryFull: "§cYour inventory is full!"
cannotCreateEnquiry: "§6[Bazaar] §cCannot create enquiry! You have too many!"
invalid: "§6[Bazaar] §eTry again"
somethingToClaim: "§6[Bazaar] §cThere are goods to claim!"
nothingToCancel: "§6[Bazaar] §cThere is nothing to cancel!"
nothingToClaim: "§6[Bazaar] §cThere is nothing to claim!"
cancelledBuyOrder: "§6[Bazaar] §cCancelled! §7Refunded §6%refund% coins §7from cancelling buy order!"
cancelledSellOffer: "§6[Bazaar] §cCancelled! §7Refunded §7%refund%§7x §r%displayname% §7from cancelling sell offer!"

noItemsToSell: "§6[Bazaar] §cYou don't have any items to sell!"

noSellOffers: "§6[Bazaar] §cCouldn't find any sell offer!"
noSellOffersAvailablePrice: "§6[Bazaar] §cThere are no sell offers available. Using predefined price"
sellOfferSetup: "§6[Bazaar] §eSell Offer Setup! §a%amount%§7x §f%displayname% §7for §6%price% coins"
sellOfferFilled: "§6[Bazaar] §eYour §aSell Offer §efor §a%amount%§7x %displayname% §ewas filled!"

noBuyOrders: "§6[Bazaar] §cCouldn't find any buy orders!"
noBuyOrdersAvailablePrice: "§6[Bazaar] §cThere are no buy orders available. Using predefined price"
buyOrderSetup: "§6[Bazaar] §eBuy Order Setup! §a%amount%§7x §f%displayname% §7for §6%price% coins"
buyOrderFilled: "§6[Bazaar] §eYour §aBuy Order §efor §a%amount%§7x %displayname% §ewas filled!"
```