---
title: "Bazaar Command: Edit"
date: 2022-12-10 11:00:00 +0100
categories: [Minecraft, Bazaar]
tags: [bazaar, command]     # TAG names should always be lowercase
---

## Main menu
Executing
```yaml
/bz edit
```
opens a GUI with all Bazaar files that can be edited.
![???](/assets/bazaar/bz_edit_main.gif "Opening the menu")

The files in the top row (located at "plugins/Bazaar/") can also be easily edited in a text editor as well as through a gui which provides suggestions and validations in the case of item editing.
By clicking one, a new GUI opens and displays all the options that are present in the file. You can easily create, delete and add options as you wish. \
![???](/assets/bazaar/bz_edit_config.gif "Edit config.yml")

## Edit category files

In the row below, all [*category*]({{site.baseurl}}/posts/bazaar-category) files are listed (1 to 5). There are two ways to edit these files. \
By right clicking one, they can be edited the same way as the ones in the top row. \
With a left click a seperate window opens, where the [*sub categories*]({{site.baseurl}}/posts/bazaar-sub-category) of the selected category are displayed. \
![???](/assets/bazaar/bz_edit_cat_1.gif "Edit Category")

An already existing sub category can be deleted with a shift click. \
A new one can be created by clicking the desired slot which corresponds to where the sub category will be placed in the Bazaar. \
To edit a sub category, click the one you want to edit. \
![???](/assets/bazaar/bz_edit_cat_2.gif "Edit Sub Category")

A new GUI will open. There are similar slots as in the GUI before, except that they now represent a [*sub sub category*]({{site.baseurl}}/posts/bazaar-sub-sub-category). \
To delete a sub sub category, shift click, to create one, click one of the empty slots and to edit one, click it. \
In addition to that, a new item is at the top. This is the item that represents the this sub category. In the Bazaar it corresponds to the following item: \
![???](/assets/bazaar/bz_sub_show.png "Sub Show Item") 

The displayed lore is not the one that will be displayed to the user, as there are two possible lores (one for a sub category with only one sub sub category and one for one with multiple products). \
So editing the lore of this item has no effect, instead take a look at *category_settings.yml#sub*. However you can still edit various other properties such as the type, displayname, enchantments, item flags, custom model data and more.

Once you click a sub sub category you want to edit, a new GUI will open. \
![???](/assets/bazaar/bz_edit_default_price.png "Default price") 

The first option lets you edit the default price. That is the unit price that will be used during enquiry creation if there are no buy orders or sell offers available. \
![???](/assets/bazaar/bz_edit_sub_sub_show.png "Sub Sub Show Item")

The next option is the item that represents this sub sub category in it's parent sub category. Editing it's lore again has no effect, instead take a look at *category_settings.yml#sub-sub*.
Editing other properties works. Note that this item will not be displayed if this is the only sub sub category in a sub category. \
In the Bazaar it corresponds to the following item: \
![???](/assets/bazaar/bz_sub_sub_show.png "Sub Sub Show")

And the last option is \
![???](/assets/bazaar/bz_edit_original.png "Original Item")

The last one is the original item, the one that will be used for transactions. With a left click you can edit it in an editor.
With a right click you can select an item from your inventory to set as the original item.