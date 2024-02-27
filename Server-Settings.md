---
title: Server Settings
description: This page outlines gameplay, world, and server settings.
published: true
date: 2023-11-11T18:30:26.365Z
tags: 
editor: undefined
dateCreated: 2023-09-24T19:21:04.901Z
---

# Plugin Configuration

<details>
  <summary> Show default file </summary>
  
```yaml
---
prefix: "&9&lIridiumSkyblock &8»"
updateChecks: true
dateTimeFormat: "EEEE, MMMM dd HH:mm:ss"
numberFormatter:
  numberAbbreviationDecimalPlaces: 2
  thousandAbbreviation: "K"
  millionAbbreviation: "M"
  billionAbbreviation: "B"
  trillionAbbreviation: "T"
  displayNumberAbbreviations: true
createRequiresName: false
preventTntGriefing: true
patreonMessage: true
minTeamNameLength: 3
maxTeamNameLength: 20
recalculateInterval: 5
forceRecalculateInterval: 1
userRanks:
  1:
    name: "Member"
    item:
      material: "STONE_AXE"
      amount: 1
      displayName: "&9&lMember"
      headData: null
      headOwner: null
      headOwnerUUID: null
      model: null
      lore: []
      slot: 12
  2:
    name: "Moderator"
    item:
      material: "IRON_AXE"
      amount: 1
      displayName: "&5&lModerator"
      headData: null
      headOwner: null
      headOwnerUUID: null
      model: null
      lore: []
      slot: 13
  3:
    name: "CoOwner"
    item:
      material: "GOLDEN_AXE"
      amount: 1
      displayName: "&2&lCoOwner"
      headData: null
      headOwner: null
      headOwnerUUID: null
      model: null
      lore: []
      slot: 14
visitor:
  name: "Visitor"
  item:
    material: "WOODEN_AXE"
    amount: 1
    displayName: "&7&lVisitor"
    headData: null
    headOwner: null
    headOwnerUUID: null
    model: null
    lore: []
    slot: 11
owner:
  name: "Owner"
  item:
    material: "DIAMOND_AXE"
    amount: 1
    displayName: "&c&lOwner"
    headData: null
    headOwner: null
    headOwnerUUID: null
    model: null
    lore: []
    slot: 15
teamInfoTitle: "&8[ &9&l%island_name% &8]"
teamInfoTitleFiller: "&8&m "
teamInfo:
- "&9Description: &7%island_description%"
- "&9Level: &7%island_level% (#%island_experience_rank%)"
- "&9Value: &7%island_value% (#%island_value_rank%)"
- "&9Online Members (%island_members_online_count%/%island_members_count%): &7%island_members_online%"
- "&9Offline Members (%island_members_offline_count%/%island_members_count%): &7%island_members_offline%"
noneChatAlias:
- "n"
- "none"
teamChatAlias:
- "i"
- "island"
teamTopSlots:
  1: 14
  2: 22
  3: 23
  4: 24
  5: 30
  6: 31
  7: 32
  8: 33
  9: 34
teamWarpSlots:
  1: 9
  2: 11
  3: 13
  4: 15
  5: 17
levelRewards:
  1:
    item:
      material: "EXPERIENCE_BOTTLE"
      amount: 1
      displayName: "&9&lLevel %island_level% Reward"
      headData: null
      headOwner: null
      headOwnerUUID: null
      model: null
      lore:
      - "&7Island Level %island_level% Rewards:"
      - "&9&l* &91000 Money"
      - "&9&l* &95 Island Crystals"
      - ""
      - "&9&l[!] &9Left click to redeem"
      slot: null
    commands: []
    money: 0.0
    bankRewards:
      Crystals: 5.0
    experience: 200
    teamExperience: 0
    sound: "ENTITY_PLAYER_LEVELUP"
  5:
    item:
      material: "EXPERIENCE_BOTTLE"
      amount: 1
      displayName: "&9&lLevel %island_level% Reward"
      headData: null
      headOwner: null
      headOwnerUUID: null
      model: null
      lore:
      - "&7Island Level %island_level% Rewards:"
      - "&9&l* &910000 Money"
      - "&9&l* &910 Island Crystals"
      - ""
      - "&9&l[!] &9Left click to redeem"
      slot: null
    commands: []
    money: 0.0
    bankRewards:
      Crystals: 10.0
    experience: 2000
    teamExperience: 0
    sound: "ENTITY_PLAYER_LEVELUP"
whitelistedWorlds: []
islandCreateTitle: "&9&lIsland Created"
islandCreateSubTitle: "&7IridiumSkyblock by Peaches_MLG"
defaultDescription: "Default island description :c"
worldName: "IridiumSkyblock"
spawnWorldName: "world"
islandTitleTop: "&9%island_name%"
islandTitleBottom: "&7%island_description%"
paster: "worldedit"
obsidianBucket: true
netherOnlyGenerator: false
endPortalPick: true
removeIslandBlocksOnDelete: false
clearInventoryOnRegen: false
clearEnderChestOnRegen: false
allowPvPOnIslands: false
distance: 151
netherUnlockLevel: 10
endUnlockLevel: 20
pasterDelayInTick: 1
pasterLimitPerTick: 10
islandCrystal:
  material: "NETHER_STAR"
  amount: 1
  displayName: "&9*** &9&lIsland Crystal &9***"
  headData: null
  headOwner: null
  headOwnerUUID: null
  model: null
  lore:
  - ""
  - "&9%amount% Island Crystals"
  - "&9&l[!] &9Right-Click to Redeem"
  slot: null
enabledWorlds:
  NORMAL: true
  NETHER: true
  THE_END: true
defaultBorderColor: "BLUE"
enabledBorders:
  BLUE: true
  RED: true
  GREEN: true
  "OFF": true
```

</details>

<details>
  <summary> Show values </summary>
  
- *prefix*: ^[String]^ The plugin's command prefix.
- *updateChecks*: ^[boolean]^ Whether the plugin will check for updates or not.
- *dateTimeFormat*: ^[String]^ The time format used for timed events, like boosters.
---
- *numberFormatter*: ^[Object]^ How numbers will be formatted for larger values.
  - *numberAbbreviationDecimalPlaces*: ^[int]^ How many decimal places a number will have.
  - *thousandAbbreviation*: ^[String]^ The character to represent a thousand.
  - *millionAbbreviation*: ^[String]^ The character to represent a million.
  - *billionAbbreviation*: ^[String]^ The character to represent a billion.
  - *trillionAbbreviation*: ^[String]^ The character to represent a trillion.
---
- *createRequiresName*: ^[boolean]^ Whether an island requires a player submitted name to be created.
- *preventTntGriefing*: ^[boolean]^ Whether to allow TNT griefing.
- *patreonMessage*: ^[boolean]^ Whether to show the patreon message to administrators.
- *minTeamNameLength*: ^[int]^ The minimum length for a team's name.
- *maxTeamNameLength*: ^[int]^ The maximum length for a team's name.
- *recalculateInterval*: ^[int]^ How often the plugin will refresh placeholders and island scores in seconds.
- *forceRecalculateInterval*: ^[int]^ How often manual recalculation can be done in seconds.
---
- *userRank*: ^[Object]^ User ranks and how they're defined.
  - *rankNumber*: ^[int]^ The rank level of the defined rank. (Can be either visitor or owner as well).
    - *name*: ^[String]^ The name of the rank.
    - *item*: ^[Object]^ The item category that determines how the permission shows up in `/is permissions`. For more information, please see our [Inventory & Menus](https://docs.iridiumdevelopment.net/en/Inventory) page.
---
- *teamInfoTitle*: ^[String]^ The title of the island shown to the player on entering.
- *teamInfoTitleFiller*: ^[String]^
- *teamInfo*: ^[String]^ The data shown to the player for the current island.
- *noneChatAlias*: ^[String]^ The chat alias to toggle island chat off.
- *teamChatAlias*: ^[String]^ The chat alias to toggle island chat on.
---
- *teamTopSlots*: ^[Object]^ What slots the leaderboard will use.
  - *topRank*: ^[in]^ The slot that the specified top rank will be displayed on.
---
- *teamWarpSlots*: ^[Object]^ What slots the islad warps will use.
  - *warpNumber*: ^[int]^ The slot that the specified warp number will be displayed on.
---  
- *levelRewards*: ^[Object]^ Level rewards configuration.
  - *level*: ^[Object]^ The level to configure.
    - *item*: ^[Object]^ The item category that determines how the permission shows up in `/is permissions`. For more information, please see our [Inventory & Menus](https://docs.iridiumdevelopment.net/en/Inventory) page.
    - *commands*: ^[String[]]^ The command(s) to run on level reward acceptance.
    - *money*: ^[double]^ The Vault currency to be added to the player's balance.
    
    - *bankRewards*: ^[List<BankItem>]^ The list of bankItems to be added to the player's island's bank.
      - *Crystals*: ^[double]^ The amount of Crystals to be added to the bank.
      - *money*: ^[double]^ The amount of Vault currency to be added to the bank.
      - *experience*: ^[double]^ The amount of experience to be added to the bank.
    - *experience*: ^[double]^ The amount of experience to be given to the player.
    - *teamExperience*: ^[double]^ The amount of experience the player's island will receive.
    - *sound*: ^[enum]^ The sound to play on levelup.
---
- *whiteListedWorlds*: ^[String[]]^ Worlds to allow missions to be completed in.
- *islandCreateTitle*: ^[String]^ The title shown when an island is created.
- *islandCreateSubTitle*: ^[String]^ The subtitle shown when an island is created.
- *defaultDescription*: ^[String]^ The default island description.
---
- *worldName*: ^[String]^ The name of the skyblock world.
- *spawWorldName*: ^[String]^ The name of the world players will spawn in initially.
- *islandTitleTop*: ^[String]^ The title shown at the top when a player enters an island.
- *islandTitleBottom*: ^[String]^ The title shown at the bottom when a player enters an island.
- *paster*: ^[String]^ The type of schematic pasting system to use. See our [Schematics](https://docs.iridiumdevelopment.net/en/Schematics) page for more details.
- *obsidianBucket*: ^[boolean]^ Whether clicking on obsidian with an emtpy bucket will return it to the player's inventory as a lava bucket.
- *endPortalPick*: ^[boolean]^ Whether shift and left-clicking an end portal frame block with any pickaxe will return it to the player's inventory.
- *removeIslandBlocksOnDelete*: ^[boolean]^ Whether the physical island will be deleted when an island is deleted.
- *clearInventoryOnRegen*: ^[boolean]^ Whether using ``/is regen`` will clear the player's inventory.
- *clearEnderChestOnRegen*: ^[boolean]^ Whether using ``/is regen`` will clear the player's ender chest.
- *allowPvPOnIslands*: ^[boolean]^ Whether to allow PvP on islands.
- *distance*: ^[int]^ The distance in blocks between islands.
- *netherUnlockLevel*: ^[int]^ The island level required to access the Nether.
- *endUnlockLevel*: ^[int]^ The island level required to access the End.
- *pasterDelayInTick*: ^[int]^ The delay of the schematics paster in ticks.
- *pasterLimitPerTick*: ^[int]^ The limit of the schematics paster per tick.
---
- *islandCrystal*: ^[Object]^ The Island Crystal's configuration.
  - *material*: ^[XMaterial]^ The item to represent the crystal.
  - *amount*: ^[int]^ How many of said item for reprsenting the crystal.
  - *displayName*: ^[String]^ The name of the crystal.
  - *headData*: ^[String]^ The data for the player skull representing the crystal.
  - *headOwner*: ^[String]^ The username of the player head owner.
  - *headOwnerUUID*: ^[String]^ The UUID of the player head owner.
  - *model*: ^[String]^ The model data for the item.
  - *lore*: ^[String]^ The tooltip shown to players on the crystal.
  - *slot*: ^[int]^ The slot for the crystal.
---
- *enabledWorlds*: ^[Object]^ The worlds allowed to generate for skyblock.
  - *dimension*: ^[boolean]^ Whether the plugin will generate a world in that dimension.
---
- *defaultBorderColor*: ^[String]^ The default color of the island border.
- *enabledBorders*: ^[Object]^ The enabled borders for islands.
  - *color*: ^[boolean]^ Whether the color is permitted for the island border.
</details>