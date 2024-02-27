---
title: Enhancements
description: This page details how to set up and use enhancements, which includes boosters and upgrades.
published: true
date: 2024-02-10T21:58:45.203Z
tags: 
editor: markdown
dateCreated: 2023-09-24T19:25:26.295Z
---

# Enhancements

"Enhancement" refers to both upgrades and boosters, as with IridiumSkyblock version 4, these are now combined together so that servers can chose whether an upgrade is a booster, or vice versa.

## Upgrades
Upgrades are enhancements that permanently apply to the island purchasing them.

## Boosters
Boosters are enhancements that temporarily apply to the island purchasing them. They have a time limit, and when the time limit expires, they no longer apply.

```yaml
flightEnhancement:
  enabled: true
  type: "BOOSTER"
  item:
    material: "FEATHER"
    amount: 1
    displayName: "&9&lFlight Booster"
    headData: null
    headOwner: null
    headOwnerUUID: null
    model: null
    lore:
    - "&7Gain access to fly."
    - ""
    - "&9&lInformation:"
    - "&9&l * &7Time Remaining: &9%timeremaining_hours% hours, %timeremaining_minutes%\
      \ minutes and %timeremaining_seconds% seconds"
    - "&9&l * &7Current Level: %current_level%"
    - "&9&l * &7Booster Cost: $%cost%"
    - ""
    - "&9&l[!] &9Left Click to Purchase Level %next_level%."
    slot: 16
  levels:
    1:
      minLevel: 5
      money: 10000
      bankCosts:
        Crystals: 5.0
      enhancementAffectsType:
      - "MEMBERS_IN_TERRITORY"
    2:
      minLevel: 10
      money: 10000
      bankCosts:
        Crystals: 5.0
      enhancementAffectsType:
      - "MEMBERS_ANYWHERE"
```
> *An example of the flight enhancement from ``enhancements.yml``.*

- *enhancement*: ^[Object]^ The enhancement being configured.
	- *enabled*: ^[boolean]^ Whether the enhancement is enabled.
  - *type*: ^[String]^ Whether the enhancement is a "BOOSTER" or an "UPGRADE".
  - *item*: ^[Object]^ The item category that determines how the enhancement shows up in `/is boosters` or `/is upgrades`. For more information, please see our [Inventory & Menus](https://docs.iridiumdevelopment.net/en/Inventory) page.
  - *levels*: ^[Object]^ The levels of the enhancement available.
  	- *level*: ^[int]^ What level is being configured.
    	- *minLevel*: ^[int]^ The island level that the player must have before purchasing the enhancement.
      - *money*: ^[double]^ The price of the enhancement in Vault currency.
      - *bankCosts*: ^[Object]^ The price of the enhancement in Bank Items.
      - *enhancementValue*: ^[Object]^ Most enhancement have a modifier value, which will be set in this field (this is different for each enhancement).
      
## List of Enhancements
<p> &nbsp </p>

|Enhancement Name| Effect | Description |
|-----|-----|-----|
|farmingEnhancement|farmingModifier|Changes the amount of stages that can be grown at once.
|spawnerEnhancement|spawnCount|Changes how many mobs will spawn out of a spawner.|
|experienceEnhancement|experienceModifier|Changes the ratio of experience gained from activities.|
|flightEnhancement|enhancementAffectsType|Changes who is affected by the flight enhancement.|
|membersEnhancement|members|Changes how many members the island can have.|
|warpsEnhancement|warps|Changes how many warps the island can have.|
|potionEnhancement|strength|Changes the strength of the potion effect specified.|
|generatorEnhancement|ores, netherOres|Allows the server to configure what spawns in the ore generators.|
|sizeEnhancement|size|Changes the currently allotted build area of the island.
|voidEnhancement|itemLossChance|Changes the percentage of items lost to the void.|