---
title: "Bazaar: category_settings.yml"
date: 2022-12-10 14:00:00 +0100
categories: [Minecraft, Bazaar]
tags: [bazaar, config]     # TAG names should always be lowercase
---

Here is a list of all options in *category_settings.yml* and their default values
```yaml
statistic:
   period: day
   range: 7
sub:
   multiple-products:
      mode:
         advanced:
            lore:
            - "&8%products% products"
            - ""
            - "&7Buy price: &6%offers_price_lowest%"
            - "&8%offers_content%&8 in &8%offers_total%&8 offers"
            - "&8%insta_buys% insta-buys in the last %period%"
            - ""
            - "&7Sell price: &6%orders_price_highest%"
            - "&8%orders_content%&8 in &8%orders_total%&8 orders"
            - "&8%insta_sells% insta-sells in the last %period%"
            - ""
            - "&eClick to view product!"
   one-product:
      mode:
         advanced:
            lore:
            - "&81 product"
            - ""
            - "&7Buy price: &6%offers_price_lowest%"
            - "&8%offers_content%&8 in &8%offers_total%&8 offers"
            - "&8%insta_buys% insta-buys in the last %period%"
            - ""
            - "&7Sell price: &6%orders_price_highest%"
            - "&8%orders_content%&8 in &8%orders_total%&8 orders"
            - "&8%insta_sells% insta-sells in the last %period%"
            - ""
            - "&eClick to view product!"
sub-sub:
   mode:
      advanced:
         lore:
         - ' '
         - '&7Buy price: &6%offers_price_lowest% coins'
         - '&8%offers_content%&8 in &8%offers_total%&8 offers'
         - '  '
         - '&7Sell price: &6%orders_price_highest% coins'
         - '&8%orders_content%&8 in &8%orders_total%&8 offers'
```