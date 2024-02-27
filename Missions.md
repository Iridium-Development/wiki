---
title: Missions
description: This page will demonstrate what types of missions are available, as well as how to set them up.
published: true
date: 2024-02-11T01:03:02.961Z
tags: 
editor: markdown
dateCreated: 2023-09-24T19:26:40.250Z
---

# Missions

```yaml
missions:
  farmer:
    missionData:
      1:
        item:
          material: "SUGAR_CANE"
          amount: 1
          displayName: "&9&lFarmer"
          headData: null
          headOwner: null
          headOwnerUUID: null
          model: null
          lore:
          - "&7Complete Island Missions to gain rewards"
          - "&7Which can be used to purchase Island Upgrades"
          - ""
          - "&9&lObjectives:"
          - "&9&l* &7Grow 10 Sugarcane: %progress_1%/10"
          - "&9&l* &7Grow 10 Wheat: %progress_2%/10"
          - "&9&l* &7Grow 10 Carrots: %progress_3%/10"
          - ""
          - "&9&lRewards"
          - "&9&l* &75 Island Crystals"
          - "&9&l* &7$1000"
          - ""
          - "&9&l * &7Time Remaining: &9%timeremaining_hours% hours %timeremaining_minutes%\
            \ minutes and %timeremaining_seconds% seconds"
          slot: null
        missions:
        - "GROW:SUGAR_CANE:10"
        - "GROW:WHEAT:10"
        - "GROW:CARROTS:10"
        completeSound: "ENTITY_PLAYER_LEVELUP"
        reward:
          item:
            material: "DIAMOND"
            amount: 1
            displayName: "&9&lFarmer Reward"
            headData: null
            headOwner: null
            headOwnerUUID: null
            model: null
            lore:
            - "&9&l Rewards"
            - "&9&l* &75 Island Crystals"
            - "&9&l* &7$1000"
            slot: null
          commands: []
          money: 1000.0
          bankRewards:
            Crystals: 5.0
          experience: 0
          teamExperience: 10
          sound: "ENTITY_PLAYER_LEVELUP"
        message: "%prefix% &7Farmer mission Completed!\n&9&l* &7+3 Island Experience\n\
          &9&l* &7+5 Island Crystals\n&9&l* &7+1000 Money\n&7/is rewards to redeem\
          \ rewards"
        missionDependencies: []
    missionType: "DAILY"
    
  dailySlots:
  - 10
  - 12
  - 14
  - 16
  customMaterialLists:
    LOGS:
    - "OAK_LOG"
    - "BIRCH_LOG"
    - "SPRUCE_LOG"
    - "DARK_OAK_LOG"
    - "ACACIA_LOG"
    - "JUNGLE_LOG"
    - "CRIMSON_STEM"
    - "WARPED_STEM"

```
> *The default farmer mission in ``missions.yml``.*

- *missions*: ^[Object]^ The missions category for configuration purposes.
	- *missionName*: ^[Object]^ The mission being configured.
  	  - *item*: ^[Object]^ The item category that determines how the mission shows up in `/is missions`. For more information, please see our [Inventory & Menus](https://docs.iridiumdevelopment.net/en/Inventory) page.
      - *missions*: ^[String]^ The missions/objectives for the configured mission.
      - *completeSound*: ^[String]^ The sound to play when a player completes a mission.
      - *reward*: ^[Object]^ The reward to be given on mission completion.
        - *item*: ^[Object]^ The item category that determines how the reward shows up in `/is rewards`. For more information, please see our [Inventory & Menus](https://docs.iridiumdevelopment.net/en/Inventory) page.
        - *commands*: ^[String]^ Any commands to be run on reward redemption.
        - *money*: ^[double]^ The Vault currecy to be awarded to the player.
        - *bankRewards*: ^[Object]^ The Bank Items to be awarded to the player (you can award Vault currency under bankRewards by using the ``money`` field.
        - *teamExperience*: ^[double]^ The amount of island experience to be given to the player's island.
        - *sound*: ^[String]^ The sound to play on reward redemption.
      - *message*: ^[String]^ The message to be sent to the player on mission completion.
  - *missionType*: ^[String]^ The mission type, can be either "DAILY", "WEEKLY", or "ONCE".
- *dailySlots*: ^[int]^ The slots that daily missions should be shown in.
- *customMaterialLists*: The category to determine custom lists of items for missions.
  
  
> Missions have three parts: the mission type, the effected item/entity/block, and the amount. A full mission should look like this:
``GROW:WHEAT:64``
Where "GROW" is the type of mission it is, "WHEAT" is the block being grown, and "64" is the amount that is required to be grown in the mission to be considered completed.
{.is-info}

For the ``customMaterialLists``, any field specified here can be referenced in your missions. For example, the LOGS custom material lists has a list of log blocks in it, and if you use ``LOGS`` instead of the name of a block in a mission, it will count if any item on the list is tracked.
You can use this to your advantage to create your own material lists to reference. Here's what this might look like with wool.

```yaml
  customMaterialLists:
    WOOL:
    - "WHITE_WOOL"
    - "PINK_WOOL"
    - "RED_WOOL"
    - "ORANGE_WOOL"
    - "YELLOW_WOOL"
    - "LIME_WOOL"
    - "GREEN_WOOL"
    - "CYAN_WOOL"
    - "LIGHT_BLUE_WOOL"
    - "BLUE_WOOL"
    - "MAGENTA_WOOL"
    - "PURPLE_WOOL"
    - "BROWN_WOOL"
    - "BLACK_WOOL"
    - "LIGHT_GRAY_WOOL"
    - "GRAY_WOOL"
```

Now, referencing "WOOL" in your missions will allow you to track if the player has affected any of the wool types. 


## List of missions
<p> &nbsp </p>


|Mission|Effect|
|-----|-----|
|MINE|Checks to see how many of the specified block the player has mined.
|GROW|Checks to see how many of the specified block the player has grown.
|PLACE|Checks to see how many of the specified block the player has placed.
|ENCHANT|Checks to see if the player has enchanted a specific item.
|KILL|Checks to see if the player has killed the specified mob.
|SMELT|Checks to see if the player has smelted the specified item.
|CRAFT|Checks to see if the player has crafted the specified item.
|FISH|Checks to see if the player has fished up the specified item.
|BREW|Checks to see if the player has brewed the specified potion.