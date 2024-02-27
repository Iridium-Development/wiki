---
title: Value & Level
description: This page describes the differences between Island Value and Island Level, and how to use both of them.
published: true
date: 2024-02-10T21:26:01.023Z
tags: 
editor: markdown
dateCreated: 2023-09-24T19:23:23.334Z
---

# Value & Level
<p> &nbsp </p>

Island Value and Island Level are similar in the fact that they both track an island metric. However, they track different statistics, and are manipulated in different ways.

## Value
Island value is based on the ``blockValues.yml`` file, where blocks and their specified values are configured. The total value of an island is based on how many of these blocks are on a player's island, and how many of them there are.

```yaml
blockValues:
  IRON_BLOCK:
    value: 3.0
    name: "&b&lIron Block"
    page: 1
    slot: 10
```
> *An example block value configuration in ``blockValues.yml``.*

- *blockValues*: ^[Object]^ The block values category.
	- *block*: ^[XMaterial]^ The name of the block to be given a value (replace with entity in spawnerValues category).
      - *value* ^[double]^ The value of the block.
      - *name*: ^[String]^ The display name of te block in the GUI.
      - *page*: ^[int]^ The page to display the block on in the GUI.
      - *slot*: ^[int]^ The slot number to display the block on in the GUI.

## Level
Island level is based on island experience, or in the configuration, ``teamExperience``. This is based on the experience provided by island missions. Level can also be used to determine whether players have access to island upgrades, boosters, their portals, etc.

```yaml
missions:
  farmer:
    missionData:
      1:
        item:
        missions:
        - "GROW:SUGAR_CANE:10"
        completeSound: "ENTITY_PLAYER_LEVELUP"
        reward:
          item:
          commands: []
          money: 1000.0
          bankRewards:
            Crystals: 5.0
          experience: 0
          teamExperience: 10
          sound: "ENTITY_PLAYER_LEVELUP"
        message: ""
        missionDependencies: []
    missionType: "DAILY"
```
> *An example of how experience can be rewarded through missions via ``teamExperience``. This has a more in depth explanation on our [Missions](https://docs.iridiumdevelopment.net/en/Missions) page.*

When an island is given island experience through mission, it is automatically applied to the island when the mission is completed.

### Settings that use Island Level

|Option|File|Effect|
|-----|-----|-----|
|netherUnlockLevel| configuration.yml | Determines the island level that players can travel through their Nether portals at.|
|endUnlockLevel| configuration.yml | Determines the island level that players can travel through their End portals at.|
|minLevel| enhancements.yml | Determines what the minimum island level the player needs before unlocking the specified enhancement.|
