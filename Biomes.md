---
title: Biomes
description: This page describes how to set up and use the Biome Shop.
published: true
date: 2024-02-18T15:13:58.664Z
tags: 
editor: markdown
dateCreated: 2023-09-24T19:28:13.782Z
---

# Biomes

Bioems are an important aspect of skyblock, as they often have special features that make it possible to retrieve specific resources that are otherwise unobtainable, and some biomes have specific mob spawns.

You can use the ``biomes.yml`` file to specify what biomes your players have access to, whether they should be charged for changing the biome, and you can organize this menu to your heart's content.

Every biome needs to be housed in a category, much like [Shop](https://docs.iridiumdevelopment.net/en/Shop) items. The example below has the ``PLAINS`` biome listed under a category titled ``Overworld``.

> Note: If a biome is dimension-specific, such as ``NETHER_WASTES``, the plugin will change the biome in the corresponding dimension.
{.is-info}

<p> &nbsp </p>

```yaml
---
categories:
  Overworld:
    item:
      material: "GRASS_BLOCK"
      amount: 1
      displayName: "&9&lOverworld"
      headData: null
      headOwner: null
      headOwnerUUID: null
      model: null
      lore: []
      slot: 11
    inventorySize: 27
items:
  Overworld:
  - name: "&9&lPlains"
    type: "GRASS_BLOCK"
    biome: "PLAINS"
    lore: []
    defaultAmount: 1
    slot: 11
    page: 1
    buyCost:
      money: 100.0
      bankItems: {}
buyPriceLore: "&aBuy Price: $%vault_cost%"
notPurchasableLore: "&cThis item cannot be purchased!"
abbreviatePrices: true
failSound: "BLOCK_ANVIL_LAND"
successSound: "ENTITY_PLAYER_LEVELUP"
biomeItemLore:
- "&9&l[!] &9Left-Click to Purchase"
```

- *categories*: ^[Object]^ The categories... category. Contains the list of categories that biomes can be sorted under.
  - *category*: ^[Object]^ The named category.
   - *item*: ^[Object]^ The item category that determines how the category shows up in `/is biomes`. For more information, please see our [Inventory & Menus](https://docs.iridiumdevelopment.net/en/Inventory) page.
   - *inventorySize*: ^[int]^ The size of the category inventory when opening (MUST BE A **MULTIPLE OF 9**).
- *items*: ^[Object]^ The category containing the shop listing.
  - *category*: ^[Object]^ The name of the category the following items will be listed under.
    - *name*: ^[String]^ The display name for the shop listing.
    - *type*: ^[XMaterial]^ The block or item listed.
    - *biome*: ^[XBiome]^ The biome available for purchase.
    - *lore*: ^[String]^ The tooltip for the biome in the shop listing.
    - *command*: ^[String]^ The command to be run on biome purchase, if any.
    - *defaultAmount*: ^[int]^ The amount of the item to be given or sold on request.
    - *slot*: ^[int]^ The slot number for the shop listing to be displayed on.
    - *page*: ^[int]^ The page number for the slot to be listed on.
    - *buyCost*: ^[Object]^ The listing price.
      - *money*: ^[double]^ The price for the listed biome in Vault currency.
      - bankItems: ^[Object]^ The price for the listed biome in bank items, such as crystals.
- *buyPriceLore*: ^[String]^ The tooltip for purchasing a biome in the shop listing.
- *notPurchasableLore*: ^[String]^ The tooltip for being unable to purchase a biome in the shop listing.
- *abbreviatePrices*: ^[boolean]^ Whether to abbreviate prices with large numbers.
- *failSound*: ^[String]^ The sound to play when a player cannot afford to buy a biome.
- *successSound*: ^[String]^ The sound to play when a player purchases a biome.
- *biomeItemLore*: ^[String]^ The tooltip appended to every biome listing.