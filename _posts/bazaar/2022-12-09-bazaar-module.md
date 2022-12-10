---
title: "Bazaar API: Module"
date: 2022-12-09 22:50:00 +0100
categories: [Minecraft, Bazaar]
tags: [bazaar, internal]     # TAG names should always be lowercase
---

# Bazaar API: Module
Nearly all of the interactions happen via a GUI:
* selecting a specific [Category]({{site.baseurl}}/posts/bazaar-category)
* creating a Sell Offer/Buy Order
* Buy/Selling instantly
* managing Enquiries

What if there is a bug or something is not configured correctly, but you do not want close the server? That's where modules come into play. A module can be enabled and disabled on the fly, so you do not need to restart the server or close the server for normal players. Each of the elements listed above are modules. You do not want players to be able to instantly buy or sell things? No problem! By toggling the *SELL_INSTANTLY_MODULE* and *BUY_INSTANTLY_MODULE* their access can be restricted! A category is not configured correctly? Toggle the *CATEGORY_[1-5]* module! Here is a list of all modules:
* *MANAGE_ENQUIRIES_MODULE*, *CLOSE_MODULE*
* *CREATE_BUY_ORDER_MODULE*, *CREATE_SELL_OFFER_MODULE*
* *BUY_INSTANTLY_MODULE*, *SELL_INSTANTLY_MODULE*
* *CAT_[1-5]*, *CAT_[1-5]_[1-18]*, *CAT_[1-5]_[1-18]_[1-9]*

The command to toggle a module is
```
/bz toggle <module>
```
and the permission is
```
bazaar.toggle
```
Once a module is toggled, the GUIs of all the players will be automatically updated, restricting or unlocking the module. Once a module has been disabled, a different item than usual will be displayed. It can be configured in *inventory.yml* under *inventory.module-disabled*.