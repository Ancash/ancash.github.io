---
title: "Bazaar: Sub Sub Category"
date: 2022-12-09 18:00:00 +0100
categories: [Minecraft, Bazaar]
tags: [bazaar, internal, module]     # TAG names should always be lowercase
---

There are a total of 9 sub categories per [Sub Category]({{site.baseurl}}/posts/bazaar-sub-category), but not all of them have to be used. 
Read [here]({{site.baseurl}}/posts/bazaar-cmd-toggle) on how to include/exclude categories without deleting them.
A sub sub category is a [Module]({{site.baseurl}}/posts/bazaar-module), so it can be enabled and disabled on the fly. It only has one item, which can be configured in *categories/category_[1-5].yml* (the number is the category) under *[1-18].subsub.[1-9].show* (the number is the sub category) or by using [*/bz set sss*]({{site.baseurl}}/posts/bazaar-cmd-set#sss) (placeholders can also be found there). To change the item that is used for transaction *[1-18].subsub.[1-9].original* in the same file can be edited or  [*/bz set original*]({{site.baseurl}}/posts/bazaar-cmd-set#original)