---
title: "Bazaar Command: toggle"
date: 2022-12-10 11:00:00 +0100
categories: [Minecraft, Bazaar]
tags: [bazaar, command, marketspace]     # TAG names should always be lowercase
---

## Creating a Marketspace
Use
```yaml 
/bz ms create <namespace>
```
Where *\<namespace>* is the [namespace]({{site.baseurl}}/posts/bazaar-namespace) you want the marketspace to be created in. \
Finally, once executed you will be prompted to input a name for the marketspace.
Permission: "bazaar.marketspace-create"

## Editing a Marketspace
Use
```yaml 
/bz ms edit <namespace>
```
Where *\<namespace>* is the [namespace]({{site.baseurl}}/posts/bazaar-namespace) the marketspace you want to edit is located in. \
Once executed, a gui will open in which you have to search for the marketspace you want to edit. You can also search by name and id.

Once a marketspace is selected, a new gui will open. Here you can edit the name and children of it. \
To iterate through the children use left click.
To delete a child entry use Q.
To add a child entry use right click. A new gui will open where you can select any root category in the namespace (no duplications allowed).
Permision: "bazaar.marketspace-edit"

## Deleting a Marketspace
Use
```yaml 
/bz ms edit <namespace>
```
Where *\<namespace>* is the [namespace]({{site.baseurl}}/posts/bazaar-namespace) the marketspace you want to edit is located in. \
Once executed, a gui will open in which you have to search for the marketspace you want to delete. You can also search by name and id. \
Once selected press the delete button in the bottom right corner.

## Opening a Marketspace
Use
```yaml 
/bz ms open <namespace>:<id> <player>
```
Where *\<namespace>* is the [namespace]({{site.baseurl}}/posts/bazaar-namespace) of the marketspace and *\<id>* the id of the marketspace. \
*\<player>* is optional. If provided the marketspace will be opened for that player.
If *\<player>* is not provided the permission is "bazaar.marketspace-open", else "bazaar.marketspace-open-other".