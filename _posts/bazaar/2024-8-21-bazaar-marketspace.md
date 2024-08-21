---
title: "Bazaar: Marketspace"
date: 2024-08-21 12:00:00 +0100
categories: [Minecraft, Bazaar]
tags: [bazaar, namespace, marketspace]     # TAG names should always be lowercase
---

A marketspace provides a container to hold a collection of specified [root categories]({{site.baseurl}}/posts/bazaar-category) that exist in the same [namespace]({{site.baseurl}}/posts/bazaar-namespace).

# Creating a Marketspace
See [here]({{site.baseurl}}/posts/bazaar-cmd-marketspace).

# Deleting a Marketspace
1. Stop the socket server
2. Delete the file "plugins/Bazaar/namespace/\<namespace>/marketspace/\<id>.yml" where \<namespace> and \<id> are the properties of the marketspace you want to delete
3. Done
