---
title: "Bazaar: Namespace"
date: 2024-08-21 12:00:00 +0100
categories: [Minecraft, Bazaar]
tags: [bazaar, namespace]     # TAG names should always be lowercase
---

A namespace provides a container to hold things like categories and enquiry data as a way to group them together logically and to help avoid conflicts with categories and enquiry data with the same name that have a different purpose. Each namespace is closed in it self and cannot interact with other namespaces.

# Creating a Namespace
Navigate to the socket server directory and open the "plugins/Bazaar/namespace" directory. \
By default it contains the "default" namespace. \
A new namespace can be created by creating a new folder like "plugins/Bazaar/namespace/test". \
Stop the socket server and start it again. Some default categories will be loaded into the new namespace. \
The console now displays all categories from the "test" namespace in the following format:
```yaml
test:<someCategoryId>
```

# Deleting a Namespace
Delete the directory of the namespace "plugins/Bazaar/namespace/\<namespace>"
