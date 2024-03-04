---
title: Schematics
description: This page goes over how to use schematics with the plugin.
published: true
date: 2024-03-04T17:19:09.431Z
tags: 
editor: markdown
dateCreated: 2024-02-27T19:05:10.703Z
---

# Schematics

You may have heard the term "schematics" when talking about blueprints or floorplans, and the same sort of idea applies here. Schematics are files that save blocks (and occassionally entities) arranged in a specific way so that they can be loaded later.

Our `desert.schem` schematic, for example, is a schematic file that has the desert island saved to it, and when you run `/is create` or `/is regen` and pick the desert option, it loads this file from the server to generate your island.

<p> &nbsp </p>

## Main Config Options

- *name*: ^[String]^ The Island type, will be used with the `/is regen` command (i.e. desert: `/is regen desert`)
	- *item*: ^[Object]^ See our [Inventories](https://docs.iridiumdevelopment.net/en/Inventory) for more details.
	- *dimension*: ^[Enum]^ Determines the dimension the schematic will be loaded in (i.e. `overworld`: ).
		- *biome*: ^[XBiome]^ Determines the biome of the island upon generation.
		- *schematicID*: ^[String]^ The name of the schematic file located in `plugins/IridiumSkyblock/schematics`.

<p> &nbsp </p>

## Offsets

Every island has a different location, and each schematic in the config has a set of coordinates that the player will spawn at. However, these coordinates are NOT EXACT. They are offsets, meaning that they are adjustment values.

For example:
```yaml
xHome: 3
yHome: 75
zHome: -1.5
yawHome: 90.0

x: + east / - west
z: - north / + south
```

With this configuration, the player will spawn 3 blocks to the east (+ x), 1.5 blocks to the north (-   z), and at y-level 75. They will also be rotated depending on yaw. All of this information can be found in the debug menu (default: **F3**).

---

- **xHome**: An offset of X, will make the player spawn x units away from their island spawn point.
- **yHome**: A direct value for Y, will make the player spawn at that height.
- **zHome**: An offset of Z, will make the player spawn x units away from their island spawn point.
- **yawHome**: This value determines what direction the player will be facing when they spawn on the island.

<p> &nbsp </p>

### Full Configuration Breakdown

<details>
  <summary> View </summary>
  
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
</details>

  <p> &nbsp </p>
  
## Using Custom Schematics

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
  
> The plugin will not accept `.iridiumschem` or `.schematic` file formats, you must
save your schematics as `.schem` files, or the plugin will not load them.
> {.is-danger}

> Your schematic should not be saved on a version higher than your server version (ex: Schematic saved in `1.18.2` while your server version is `1.17.1`) as this may cause issues, including (but not limited to) the island not generating at all.
{.is-warning}
  
<p> &nbsp </p>
  
## Using World Edit
You can change how the plugin handles pasting your islands using a third party plugin like World Edit or FAWE, if you have them installed. By default, the paste system is set to use our internal, async one.
  
You can change which paste system the plugin is using by changing `paster: "worldedit"` in `configuration.yml`. See our [General Settings](https://docs.iridiumdevelopment.net/en/Server-Settings) page for more details.

|Plugin|Setting|
|------|-------|
|IridiumSkyblock (internal)|`internalAsync`|
|World Edit|`worldEdit`|
|Async World Edit|`fawe`|
|Fast Async World Edit|`fawe`|