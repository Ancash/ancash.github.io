---
title: "Bazaar: Marketspace"
date: 2024-08-21 12:00:00 +0100
categories: [Minecraft, Bazaar]
tags: [bazaar, namespace, marketspace]     # TAG names should always be lowercase
---

A marketspace provides a container to hold a collection of specified [root categories]({{site.baseurl}}/posts/bazaar-category) that exist in the same [namespace]({{site.baseurl}}/posts/bazaar-namespace).

## Creating a Marketspace
See [here]({{site.baseurl}}/posts/bazaar-cmd-marketspace).

## Deleting a Marketspace
See [here]({{site.baseurl}}/posts/bazaar-cmd-marketspace).

## Editing a Marketspace
See [here]({{site.baseurl}}/posts/bazaar-cmd-marketspace).

## Default Marketspace
Each [namespace]({{site.baseurl}}/posts/bazaar-namespace) has a default marketspace which contains all its' [root categories]({{site.baseurl}}/posts/bazaar-root-category).
The id is *-1*. It is the marketspace that is opened when using
```yaml
/bz open <namespace>
/bz open <namespace> <player>
```