---
title: Schematics
description: This page goes over how to use schematics with the plugin.
published: true
date: 2023-10-22T17:58:06.669Z
tags: 
editor: undefined
dateCreated: 2023-09-24T19:23:58.777Z
---

## Properties

```yaml
desert:
    item:
    regenCost:
      money: 1000.0
      bankItems: {}
    xHome: -0.5
    yHome: 89.0
    zHome: -0.5
    yawHome: 90.0
    overworld:
      biome: "DESERT"
      schematicID: "desert.schem"
      islandHeight: 90.0
      ignoreAirBlocks: true
```

- **Schematic**: ^[String]^ The name of the schematic according to the plugin.
	- *item*: ^[Object]^ The item category that determines how the permission shows up in `/is permissions`. For more information, please see our [Inventory & Menus](https://docs.iridiumdevelopment.net/en/Inventory) page.
  - *regenCost*: ^[Object]^ The cost of regenerating a player's island with this schematic.
  	- *money*: ^[double]^ Vault currency cost.
    - *bankItems*: ^[List<BankItem>]^ The list of BankItems and the cost associated with them.
  - ***x**Home*: ^[double]^ An offset of X, will make the player spawn x units away from their original spawn point (If the player originally spawns at 5 and the schematic has an offset of -1, they would then spawn at 4).
  - ***y**Home*: ^[double]^ A direct value for Y, will make the player spawn at that height.
  - ***z**Home*: ^[double]^ An offset of Z, will make the player spawn x units away from their original spawn point (If the player originally spawns at 6 and the schematic has an offset of 2, they would then spawn at 8).
  - ***yawHome***: ^[double]^ This value determines what direction the player will be facing when they spawn on the island.
  - *dimension*: ^[enum]^ Dimension-specific values that affect each individual schematic.
  	- *biome*: ^[XBiome]^ The biome specified for the island to be generated in.
    - *schematicID*: ^[String]^ The name of the file to be loaded in as the schematic (should end in ``.schem``).
    - *islandHeight*: ^[double]^ The height at which to spawn the schematic.
    - *ignoreAirBlocks*: ^[boolean]^ Whether to ignore air blocks that happen to be a part of a schematic when generating.

## Using Custom Schematics

### Importing
Importing your WorldEdit schematics to IridiumSkyblock is as easy as copying the schematic and pasting it in the plugin's schematics folder: ``/plugins/IridiumSkyblock/schematics``, then updating your ``schematics.yml`` file by specifying the schematic's file name under ``schematicID``.

Make sure you're running the latest version of WorldEdit and IridiumSkyblock, and set your ``paster`` setting in ``configuration.yml`` appropriately (see our [Server Settings]() page for more information).

<details>
  <summary> View Example of Custom Schematic </summary>

  ```yaml
---
schematics:
  myCustomSchematic: 
    item:
      material: "PLAYER_HEAD"
      amount: 1
      displayName: "&b&lCustom Island"
      headData: null
      headOwner: "Notch"
      headOwnerUUID: null
      model: null
      lore:
      - "&7My Custom Schematic."
      slot: 14
      regenCost:
      money: 100
      bankCost: {
        Crystals: 15
      }
    xHome: 0.5
    yHome: 96
    zHome: 0.5
    yawHome: 100
    overworld:
      biome: "PLAINS"
      schematicID: "customSchematic.schem"
      islandHeight: 90.0
      ignoreAirBlocks: true
    nether:
      biome: "NETHER_WASTES"
      schematicID: "customSchematic_nether.schem"
      islandHeight: 90.0
      ignoreAirBlocks: true
    end:
      biome: "THE_END"
      schematicID: "customSchematic_end.schem"
      islandHeight: 90.0
      ignoreAirBlocks: true
```
</details>
  
<center>

  ![schematics-menu-example.png](/schematics-menu-example.png)
  
</center>
  
> *A custom schematic menu. This menu will not show up on servers that only have a single option to choose from.*