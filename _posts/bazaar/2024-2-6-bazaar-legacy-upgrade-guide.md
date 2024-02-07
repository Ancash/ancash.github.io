---
title: "Bazaar Legacy Upgrade Guide "
date: 2024-02-06 00:00:00 +0100
categories: [Minecraft, Bazaar]
tags: [bazaar]
---


# Upgrading from Bazaar <7.X.X to 7.X.X

A [Socket Server](https://www.spigotmc.org/resources/sockets.94930/) is now mandatory in order to run Bazaar.
All Enquiry and Category data will be saved in the Bazaar directory of the Socket Server (plugins/Bazaar).

## Converting legacy Enquiry Files
If you are already using a socket server, you have nothing to do.

If not, copy the whole "plugins/Bazaar/player" folder from the minecraft server
directory and move it to the "plugins/Bazaar/player" folder of the socket server.
Up on server start all Enquiry files will be checked for legacy content and upgraded if needed.

## Converting legacy Category Files
All category files you want to convert need to have the following naming convention:
```category_{i}.yml``` where ```{i}``` is any number between 1 and 5 (both inclusive).

Open the "plugins/Bazaar/categories" folder in the Socket Server directory and move all the category files there.
Up on server start all Category files will be checked for legacy content and upgraded if needed.