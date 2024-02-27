---
title: Island Settings
description: This page details how island settings work, what settings are currently availble, and member management.
published: true
date: 2024-02-10T20:29:38.273Z
tags: 
editor: markdown
dateCreated: 2023-09-24T18:33:32.160Z
---

# Island Settings
<p> &nbsp </p>

## Setting Configuration

```yaml
teamJoining:
  item:
    material: "GUNPOWDER"
    amount: 1
    displayName: "&9Island Type"
    headData: null
    headOwner: null
    headOwnerUUID: null
    model: null
    lore:
    - "&7Set your Island joining method."
    - ""
    - "&9&lValue"
    - "&7%value%"
    slot: 10
  displayName: "JoinType"
  defaultValue: "Private"
  enabled: true
```

> *The default configuration for the teamJoining setting in ``settings.yml``.*

- *islandSetting*: ^[Object]^ The Island Setting's configuration.
  - *item*: ^[Object]^ The item category that determines how the permission shows up in `/is permissions`. For more information, please see our [Inventory & Menus](https://docs.iridiumdevelopment.net/en/Inventory) page.
  - *displayName*: ^[String]^ The name of the setting in the GUI.
  - *defaultValue*: ^[String]^ The default setting value for new islands.
  - *enabled*: ^[boolean]^ Whether the setting is enabled.
  
## Current Settings
<p> &nbsp </p>

|Setting|Values|
|-----|------|
|teamJoining|"Public" or "Private"|
|teamValue|"Public" or "Private"|
|mobSpawning| "Enabled" or "Disabled"|
|leafDecay|"Enabled" or "Disabled"|
|iceForm|"Enabled" or "Disabled"|
|fireSpread|"Enabled" or "Disabled"|
|cropTrample|"Enabled" or "Disabled"|
|weather| "Server", "Sunny", "Raining"|
|time| "Server", "Sunrise", "Day", "Morning", "Noon", "Sunset", "Night", "Midnight"|
|entityGrief| "Enabled" or "Disabled"|
|tntDamage| "Enabled" or "Disabled"|
|visiting| "Enabled" or "Disabled"|

