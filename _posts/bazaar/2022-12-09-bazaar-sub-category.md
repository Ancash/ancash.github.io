---
title: "Bazaar API: Sub Category"
date: 2022-12-09 18:00:00 +0100
categories: [Minecraft, Bazaar]
tags: [bazaar, internal, module]     # TAG names should always be lowercase
---

# Bazaar API: Sub Category

There are a total of 18 sub categories per [Category]({{site.baseurl}}/posts/bazaar-category), but not all of them have to be used. 
Read [here]({{site.baseurl}}/posts/bazaar-cmd-open) and [here]({{site.baseurl}}/posts/bazaar-cmd-toggle) on how to include/exclude categories without deleting them.
A sub category is a [Module]({{site.baseurl}}/posts/bazaar-module), so it can be enabled and disabled on the fly. It can have up to 9 [Sub Sub Categories]({{site.baseurl}}/posts/bazaar-sub-sub-category). It is represented by an item, which can be configured in *categories/category_[1-5].yml* (the number is the category) under *[1-18].sub* (the number is the sub category) or by using the [set command]({{site.baseurl}}/posts/bazaar-cmd-set).
There are some placeholders which can be used:
* *%offers_content%* (the sum of the content of all the Sell Offers in its' sub sub categories)
* *%offers_total%* (how many Sell Offers are in its' sub sub categories)
* *%orders_content%* (the sum of the content of all the Buy Orders in its' sub sub categories)
* *%orders_total%* (how many Buy Orders are in its' sub sub categories)