---
title: "Bazaar: Refund"
date: 2023-07-24 12:00:00 +0100
categories: [Minecraft, Bazaar]
tags: [bazaar]     # TAG names should always be lowercase
---

Although highly unlikely, in the case an enquiry is corrupted (e.g. through a bug), Bazaar tries to recover that enquiry. \
Note that Bazaar does not know in which state the enquiry was before it has been corrupted. \
Now the refund settings specified in [config.yml#refund]({{site.baseurl}}/posts/bazaar-config) come into play. \
```yaml
refund:
   sell-offer:
      refund-type: EDUCT
      factor: 1
   buy-order:
      refund-type: EDUCT
      factor: 1
```

There are three refund types
* NONE
* EDUCT
* PRODUCT

## None
As the name implies, no refund is given.

## Educt
The input will be refunded.
Meaning in the case of a [Sell Offer]({{site.baseurl}}/posts/bazaar-sell-offer), the items that were used to create it will be refunded, \
and the coins that were used to create a [Buy Order]({{site.baseurl}}/posts/bazaar-buy-order) will be used to refund a Buy Order.

## Product
The output will be refunded.
Meaning in the case of a Sell Offer, the coins that would fill it will be refunded, \
and the items that would fill a Buy Order will be refunded in the case of a Buy Order.