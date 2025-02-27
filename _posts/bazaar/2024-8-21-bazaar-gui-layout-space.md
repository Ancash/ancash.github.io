---
title: "Bazaar: GUI Layout Space"
date: 2025-02-26 12:00:00 +0100
categories: [Minecraft, Bazaar]
tags: [bazaar, gui]     # TAG names should always be lowercase
---

A GUILayoutSpace (GLS) is a collection of configuration files that represent nearly every gui provided by the bazaar. Here is a list of customizable GUIs in a GLS which are all part of the default gls (default-layout):\
![???](/assets/bazaar/gls-root-default.png "default root layout")
![???](/assets/bazaar/gls-fertile-default.png "default fertile layout")
![???](/assets/bazaar/gls-infertile-default.png "default infertile layout")
![???](/assets/bazaar/gls-manage-enquiries-default.png "default manage enquiries layout")

Here is a different root category inside the classic-layout, which can be opened with [*/bz open classic-layout*]({{site.baseurl}}/posts/bazaar-cmd-open).
![???](/assets/bazaar/gls-root-classic.png "classic root layout")

Everything from the title format, size to item arrangement and exclusion/inclusion can configured.
```yaml
id: classic-root
title: '{bazaar_cat-name_{bazaar_ns}:{bazaar_cur-cat}}'
size: '54'
vars:
  - cur-page:int:1
  - max-page:int:1
content:
  - slots: '45'
    item: bazaar_search
  - slots: '48'
    item: bazaar_sell-inventory
  - slots: '49'
    item: bazaar_close
  - slots: '50'
    item: bazaar_manage-enquiries
  - slots: 0;9;18;27;36
    item: bazaar_root-categories
    on-click:
      - condition: '{bazaar_is-root}'
        action: bazaar_open_classic-root
      - condition: '{bazaar_is-fertile}'
        action: bazaar_open_classic-fertile
      - condition: '{bazaar_is-infertile}'
        action: bazaar_open_classic-infertile
  - slots: 11..16;20..25;29..34;38..43
    item: bazaar_child-categories
    on-click:
      - condition: '{bazaar_is-fertile}'
        action: bazaar_open_classic-fertile
      - condition: '{bazaar_is-infertile}'
        action: bazaar_open_classic-infertile
  - slots: '{bazaar_size} - 1'
    item: bazaar_next-page
    condition: '{bazaar_var_cur-page} < {bazaar_var_max-page}'
  - slots: '{bazaar_size} - 9'
    item: bazaar_prev-page
    condition: '{bazaar_var_cur-page} > 1'
```
As a first advice do not touch any values in *vars*.

The most important part are the *content* entries.
The basic syntax is:
```yaml
slots: <slots>
item: <item>
```
Where \<slots> contains singular slots like '12' or specific ranges like '0..8'. Combinations are possible, seperated by ';' and order matters.
The \<item> is like a placeholder for an item that is computed depending on the context. The context basically is which [namespace]({{site.baseurl}}/posts/bazaar-namespace), [marketspace]({{site.baseurl}}/posts/bazaar-namespace) etc. so nothing for you to worry about.
Here is a list of all items:
- bazaar_prev-page
- bazaar_next-page
- bazaar_close
- bazaar_back
- bazaar_manage-enquiries
- bazaar_sell-inventory
- bazaar_search
- bazaar_graphs
- bazaar_transaction-item
- bazaar_buy-instantly
- bazaar_sell-instantly
- bazaar_create-sell-offer
- bazaar_create-buy-order
- bazaar_child-categories

Depending on the context some items cannot be computed. For example a [root category]({{site.baseurl}}/posts/bazaar-root-category) cannot have a transaction item.
