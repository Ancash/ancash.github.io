---
title: "Bazaar API: First Steps"
date: 2022-12-09 12:00:00 +0100
categories: [Minecraft, Bazaar]
tags: [bazaar, api]     # TAG names should always be lowercase
---

# Bazaar API: First Steps

First, you'll want to register Bazaar as a dependency of your plugin.  
To do that, open the *plugin.yml* of your plugin, then add *Bazaar* as a dependency to the *depend* option.
```yaml
depend: [Bazaar]
```
To use the [api](/doc/bazaar-api/index.html) you have to import the *Bazaar.jar* file to your project.
The source code can be found [here](https://github.com/Ancash/BazaarAPI).

Now, to get the api:
```java
import de.ancash.bazaar.Bazaar;
...
ICoreDAO coreDAO = Bazaar.getAPI();
```

The return object provides access to all the api functions:
* [ICoreDAO]({{site.baseurl}}/posts/bazaar-api-icoredao) (access to all other DAOs, and more)
* [ITransactionDAO]({{site.baseurl}}/posts/bazaar-api-itransactiondao) (used to create enquiries and manage instant sell/buy actions)
* [IPlaceholderDAO]({{site.baseurl}}/posts/bazaar-api-iplaceholderdao) (not really inteded for third party use, you can still use this to automatically replace placeholders)
* [IStatisticsDAO]({{site.baseurl}}/posts/bazaar-api-istatisticsdao) (provides access to statistics about all recorded transactions)
  
It does not matter, whether Bazaar is configured to support sockets, or not. However, the plugin is designed to be efficient and fast to support a lot of transaction per time unit and since communication with a remote server can be time consuming, all method calls should be made asynchronously. All methods are by design thread safe, hence it's possible for a method call to have to wait until another method call finishes (thus making all calls possibly blocking).