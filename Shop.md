---
title: Shop
description: This page details how to set up and use the included shop.
published: true
date: 2024-02-11T01:21:48.539Z
tags: 
editor: markdown
dateCreated: 2023-09-24T19:27:32.750Z
---

# Shop

```yaml
---
categories:
  Blocks:
    item:
      material: "GRASS_BLOCK"
      amount: 1
      displayName: "&9&lBlocks"
      headData: null
      headOwner: null
      headOwnerUUID: null
      model: null
      lore: []
      slot: 12
    inventorySize: 54
items:
  Blocks:
  - name: "&9&lGrass Block"
    type: "GRASS_BLOCK"
    lore: []
    command: null
    defaultAmount: 1
    slot: 10
    page: 1
    buyCost:
      money: 100.0
      bankItems: {}
    sellCost:
      money: 10.0
      bankItems: {}
buyPriceLore: "&aBuy Price: $%vault_cost%"
sellRewardLore: "&cSelling Reward: $%vault_reward%"
notPurchasableLore: "&cThis item cannot be purchased!"
notSellableLore: "&cThis item cannot be sold!"
abbreviatePrices: true
dropItemWhenFull: false
failSound: "BLOCK_ANVIL_LAND"
successSound: "ENTITY_PLAYER_LEVELUP"
shopItemLore:
- " "
- "&9&l[!] &9Left-Click to Purchase %amount%, Shift for 64"
- "&9&l[!] &9Right Click to Sell %amount%, Shift for 64"
```

- *categories*: ^[Object]^ The categories... category. Contains the list of categories that items can be sorted under.
  - *category*: ^[Object]^ The named category.
   - *item*: ^[Object]^ The item category that determines how the category shows up in `/is shop`. For more information, please see our [Inventory & Menus](https://docs.iridiumdevelopment.net/en/Inventory) page.
   - *inventorySize*: ^[int]^ The size of the category inventory when opening (MUST BE A **MULTIPLE OF 9**).
- *items*: ^[Object]^ The category containing the shop listing.
  - *category*: ^[Object]^ The name of the category the following items will be listed under.
    - *name*: ^[String]^ The display name for the shop listing.
    - *type*: ^[XMaterial]^ The block or item listed.
    - *lore*: ^[String]^ The tooltip for the item in the shop listing.
    - *command*: ^[String]^ The command to be run on item purchase, if any.
    - *defaultAmount*: ^[int]^ The amount of the item to be given or sold on request.
    - *slot*: ^[int]^ The slot number for the shop listing to be displayed on.
    - *page*: ^[int]^ The page number for the slot to be listed on.
    - *buyCost*: ^[Object]^ The listing price.
      - *money*: ^[double]^ The price for the listed item in Vault currency.
      - bankItems: ^[Object]^ The price for the listed item in bank items, such as crystals.
    - *sellCost*: ^[Object]^ The listing sell price.
      - *money*: ^[double]^ The sellprice for the listed item in Vault currency.
      - bankItems: ^[Object]^ The sellprice for the listed item in bank items, such as crystals.
- *buyPriceLore*: ^[String]^ The tooltip for purchasing an item in the shop listing.
- *sellRewardLore*: ^[String]^ The tooltip for selling an item in the shop listing.
- *notPurchasableLore*: ^[String]^ The tooltip for being unable to purchase an item in the shop listing.
- *notSellableLore*: ^[String]^ The tooltip for being unable to sell an item in the shop listing.
- *abbreviatePrices*: ^[boolean]^ Whether to abbreviate prices with large numbers.
- *dropItemWhenFull*: ^[boolean]^ Whether to drop shop items when player's inventory is full.
- *failSound*: ^[String]^ The sound to play when a player cannot afford to buy an item.
- *successSound*: ^[String]^ The sound to play when a player purchases an item.
- *shopItemLore*: ^[String]^ The tooltip appended to every shop listing.