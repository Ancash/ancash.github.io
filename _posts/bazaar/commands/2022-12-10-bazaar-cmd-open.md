---
title: "Bazaar Command: open"
date: 2022-12-10 11:00:00 +0100
categories: [Minecraft, Bazaar]
tags: [bazaar, command]     # TAG names should always be lowercase
---

## No args
***/bz open*** \
opens the Bazaar for the player that executed the command.
The permission is: *bazaar.open*

## \<player>
***/bz open \<player>*** \
opens the Bazaar for the specified player. 
The command sender has to have the permission: *bazaar.openo*

## include \<1-5> \<1-5> \<...>
***/bz open include \<1-5> \<1-5> \<...>*** \
opens the Bazaar for the player that executed the command but only includes the specified categories in the GUI.\
The excluded categories are replaced by the background item.\
If no categories are included, nothing happens.\
The permission is: *bazaar.open*

## \<player> include \<1-5> \<1-5> \<...>
***/bz open \<player> include \<1-5> \<1-5> \<...>*** \
opens the Bazaar for the specified player but only includes the specified categories in the GUI.\
The excluded categories are replaced by the background item.\
If no categories are included, nothing happens.\
The permission is: *bazaar.openo*

## exclude \<1-5> \<1-5> \<...>
***/bz open exclude \<1-5> \<1-5> \<...>*** \
opens the Bazaar for the player that executed the command but excludes the specified categories in the GUI.\
The excluded categories are replaced by the background item.\
If all categories are excluded, nothing happens.\
The permission is: *bazaar.open*

## \<player> exclude \<1-5> \<1-5> \<...>
***/bz open \<player> exclude \<1-5> \<1-5> \<...>*** \
opens the Bazaar for the specified player but excludes the specified categories in the GUI.\
The excluded categories are replaced by the background item.\
If all categories are excluded, nothing happens.\
The permission is: *bazaar.openo*