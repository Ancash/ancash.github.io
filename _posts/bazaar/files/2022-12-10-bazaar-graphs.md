---
title: "Bazaar: graphs.yml"
date: 2022-12-10 14:00:00 +0100
categories: [Minecraft, Bazaar]
tags: [bazaar, config]     # TAG names should always be lowercase
---

Here is a list of all options in *graphs.yml* and their default values
```yaml
y-scale: 10
title: '%prev% §r -> §eGraphs'
time-unit:
  year:
    long-pl: years
    short: y
    enabled: true
    long: year
  hour:
    long-pl: hours
    short: h
    enabled: true
    long: hour
  day:
    long-pl: days
    short: d
    enabled: true
    long: day
  month:
    long-pl: months
    short: m
    enabled: true
    long: month
range:
  last-hours: 24
  last-months: 12
  last-days: 31
  last-years: 10
items:
  buy-order:
    volume:
      UnspecificMeta:
        Lore:
        - '&7The total volume (amount of items) of Buy'
        - '&7Orders.'
        - ''
        - '%graph%'
        - ''
        - '&eClick to switch span'
        DisplayName: '&aBuy Orders Volume &r%period%'
      Amount: 1
      NBTNexusItem:
        type: SERIALIZED
      XMaterial: PAPER
    money:
      UnspecificMeta:
        Lore:
        - '&7The price at which Buy Orders have been filled.'
        - ''
        - '%graph%'
        - ''
        - '&eClick to switch span'
        DisplayName: '&aBuy Price &r%period%'
      Amount: 1
      NBTNexusItem:
        type: SERIALIZED
      XMaterial: PAPER
  sell-offer:
    volume:
      UnspecificMeta:
        Lore:
        - '&7The total volume of Sell Offers.'
        - ''
        - '%graph%'
        - ''
        - '&eClick to switch span'
        DisplayName: '&aSell Offers Volume &r%period%'
      Amount: 1
      NBTNexusItem:
        type: SERIALIZED
      XMaterial: PAPER
    money:
      UnspecificMeta:
        Lore:
        - '&7The price at which Sell Offers have been filled.'
        - ''
        - '%graph%'
        - ''
        - '&eClick to switch span'
        DisplayName: '&aSell Price &r%period%'
      Amount: 1
      NBTNexusItem:
        type: SERIALIZED
      XMaterial: PAPER
  buy-instantly:
    volume:
      UnspecificMeta:
        Lore:
        - '&7The quantity of items which have been'
        - '&7instantly bought.'
        - ''
        - '%graph%'
        - ''
        - '&eClick to switch span'
        DisplayName: '&aInstant Buy Volume &r%period%'
      Amount: 1
      NBTNexusItem:
        type: SERIALIZED
      XMaterial: PAPER
    money:
      UnspecificMeta:
        Lore:
        - '&7The total coins spent on instantly buying items.'
        - '&7items.'
        - ''
        - '%graph%'
        - ''
        - '&eClick to switch span'
        DisplayName: '&aInstant Buy Moving Coins &r%period%'
      Amount: 1
      NBTNexusItem:
        type: SERIALIZED
      XMaterial: PAPER
  sell-instantly:
    volume:
      UnspecificMeta:
        Lore:
        - '&7The quantity of items which have been'
        - '&7instantly sold (which filled Buy Orders)'
        - ''
        - '%graph%'
        - ''
        - '&eClick to switch span'
        DisplayName: '&aInstant Sell Volume &r%period%'
      Amount: 1
      NBTNexusItem:
        type: SERIALIZED
      XMaterial: PAPER
    money:
      UnspecificMeta:
        Lore:
        - '&7The total coins gained from instantly selling'
        - '&7items.'
        - ''
        - '%graph%'
        - ''
        - '&eClick to switch span'
        DisplayName: '&aInstant Sell Moving Coins &r%period%'
      Amount: 1
      NBTNexusItem:
        type: SERIALIZED
      XMaterial: PAPER
  selected-prefix: §e
  not-selected-prefix: §7
```