---
title: "Bazaar: DiscordSRV"
date: 2023-07-24 12:00:00 +0100
categories: [Minecraft, Bazaar]
tags: [bazaar]     # TAG names should always be lowercase
---

When player interact with the Bazaar, certain actions trigger events such as EnquiryCreateEvent, EnquiryCancelEvent, SellInstantlyEvent and BuyInstantlyEvent.

These events can be logged in a Discord Text Channel. \
The following configuration file *discordsrv.yml* provides the necessary options to configure which events you want to log where.
```yaml
enquiry-event-channel: ""
instant-transaction-event-channel: ""
overview-channel: ""
```
The EnquiryCreateEvent and EnquiryCancelEvent will be logged in the *enquiry-event-channel*. \
The SellInstantlyEvent and BuyInstantlyEvent will be logged in the *instant-transaction-event*.

The *overview-channel* is a bit different. \
Here, one embed message will sent and its' id will be saved in the *discordsrv.yml* file. \
It contains a short summary of all the available Enquiries. \
Note that only the Sell and Buy Price will be displayed due to message length limitations. \
The Buy Price will only be displayed if there is something to buy. Same goes for Sell Price. \
Once any of the events above takes place, the *overview-message* will be updated to the current state of the Bazaar. \
The time of the last updated will be saved in the message as well
![Overview Message](/assets/bazaar/bz_dc.png "Overview Message")

**Note**
If the socket option is enabled, all events that happen on a server will be published to all other servers, \
thus only one Bazaar Instance on a MC Server needs to be configured to log events to Discord.