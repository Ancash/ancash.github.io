---
title: "Bazaar API: Category"
date: 2022-12-09 18:00:00 +0100
categories: [Minecraft, Bazaar]
tags: [bazaar, internal, module]     # TAG names should always be lowercase
---

# Bazaar API: Category

By default there are a total of 5 categories. A category is a [Module]({{site.baseurl}}/posts/bazaar-module), so it can be enabled and disabled on the fly. It can have up to 18 [Sub Categories]({{site.baseurl}}/posts/bazaar-sub-category). It is represented by an item, which can be configured in *inventory.yml* under *inventory.categories.[1-5]*. For this item there are no placeholders available. Once an category has been selected, the item will be enchant and thus start glowing, indicating which category is currently selected.