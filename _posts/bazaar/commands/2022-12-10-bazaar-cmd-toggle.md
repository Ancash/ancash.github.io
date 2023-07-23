---
title: "Bazaar Command: toggle"
date: 2022-12-10 11:00:00 +0100
categories: [Minecraft, Bazaar]
tags: [bazaar, command, module]     # TAG names should always be lowercase
---

This command allows you to toggle specific [Modules]({{site.baseurl}}/posts/bazaar-module)

Here is a list of all modules:
* MANAGE_ENQUIRIES_MODULE
* CREATE_BUY_ORDER_MODULE
* BUY_INSTANTLY_MODULE
* GRAPH_MODULE
* SELL_INSTANTLY_MODULE
* BACK_MODULE
* VIEW_GRAPHS_MODULE
* CREATE_SELL_OFFER_MODULE
* CLOSE_MODULE
* CAT_[1-5]
* CAT_[1-5]_[1-18]
* CAT_[1-5]\_[1-18]_[1-9]

To toggle a module you have to use the command ***/bz toggle \<module>***

The permission is: *bazaar.toggle*

Players in the Bazaar will see the changes instantly. So for example if they are in the main menu, and the *MANAGE_ENQUIRIES_MODULE* is toggled, they won't be able to click the *Manage Enquiries* item, instead they will see a predefined item, which does not have any functionality.
This feature is actually quiet powerfull. It also you to disable features you do not want to include, that are not configured correctly or that do not function as intended (bug).