---
title: Inventory & Menus
description: This page shows how to edit the different plugin menus.
published: true
date: 2024-02-11T01:36:13.791Z
tags: 
editor: markdown
dateCreated: 2023-09-24T19:29:21.740Z
---






## Menu Slots
Slots are spaces in the menus of Minecraft that hold items. This often includes chests, the player inventory, and the hot-bar at the bottom of the screen. Minecraft's basic inventory menu can hold a maximum of 54 slots.

<center>

  ![menu-slots-example.png](/menu-slots-example.png)
  
</center>

### How Slots are Counted
In Java, counting typically starts from zero, instead of math's one. It can be a bit confusing at times, but it's important to keep track of. IridiumSkyblock uses a similar counting system to count its slot numbers.
Here, you can see how Iridium Skyblock handles slot numbers. The first slot in the corner is considered to be slot 0 instead of slot 1. A simple conversion for your slot number needs would be to subtract 1 from each slot you plan to fill. slot = space number - 1.

## Item Entries
Item Entries are the items that represent certain parts of the GUI. This includes menu navigation, purchasable items in the shop, the island upgrades menu, and every interact-able part of the GUI included with the plugin.

## Background Items
Background items are exactly that: items placed over the unused slots to provide a visual effect. In the default configuration, this includes glass panes that cover the unused slots and act as a filler to better highlight the Item Entries.

## Menu Titles
You may notice in the above screenshot that the menu has a title. This can be set for any section of the GUI. You can find more information on that here. 
In this section of the wiki, we'll explain how the item: config option works. 
This should be the same with each config file that has this option, and is responsible for how the item in the GUI will look.

```yaml
item:
  material: "GRASS_BLOCK"
  amount: 1
  displayName: "&9&lBlocks"
  headData: null
  headOwner: null
  headOwnerUUID: null
  model: null
  lore: []
  slot: 1
```

- *material*: ^[XMaterial]^ The item to be shown in the GUI.
- *amount*: *[int]^ The amount of the item to display.
- *displayName*: ^[String]^ The display name of the item in the GUI.
- *headData*: ^[String]^ Head data to display on a player head, if applicable.
- *headOwner*: ^[String]^ The username of the player for a player head, if applicable.
- *headOwnerUUID*: ^[String]^ The UUID of the player for a player head, if applicable.
- *model*: ^[int]^ The model data for the item.
- *lore*: ^[String]^ The tooltip for the item in the GUI.
- *slot*: ^[int]^ The slot that the item should appear in on the GUI.

