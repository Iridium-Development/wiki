---
title: Features
description: Features in IridiumSkyblock
published: true
date: 2024-02-18T15:36:23.687Z
tags: 
editor: markdown
dateCreated: 2023-04-01T21:29:03.116Z
---

# World

<p> &nbsp </p>

## Dimensional Islands

Yes, you read that right. IridiumSkyblock has the option to generate islands in *all three dimensions*, and players can travel between them and do missions unique to that dimension.

You can configure the plugin to lock players out of dimensions until they've reached a certain Island Level.

<details>
  <summary> The Overworld </summary>
  
  The starting world, this is where players will start their IridiumSkyblock journey.
  
  It's recommended that you give players starting supplies dependent on the difficulty you want, as the starting items are crucial to the beginning stages of skyblock.
  
---

![jungle.png](/jungle.png)
> *The default Jungle Island - Overworld schematic.*
  
</details>

<details>
  <summary> The Nether </summary>

Once players reach or unlock the Nether, they can access the **Basalt Generator**. This generator works just like the Cobblestone Generator, and can be configured with a different set of blocks to generate.
  
The schematics you select for the Nether should have items for this generator in the chest.
  
  
---

![jungle_nether.png](/jungle_nether.png)
> *The default Jungle Island - Nether schematic.*
  
</details>

<details>
  <summary> The End </summary>
Once players reach or unlock the End, they have reached the final world. All they need to do is build their own End Portal - how they get the frame is up to you!

  <details>
    <summary> End Portal Frame Repositioning </summary>
    
When the config option "endPortalPick" is set to true (`endPortalPick: true` in `config.yml`), a player can **sneak** and **left-click** on an **end portal frame** with **any pickaxe** to break the frame and return it to their inventory. Convenient for moving the end portal, and for fixing mistakes in building it.
    
  </details>
  
---

![jungle_end.png](/jungle_end.png)
> *The default Jungle Island - End schematic.*
  
</details>

Three times the space, three times the fun.

<p> &nbsp </p>

## World Generation

While many people take the definition of "skyblock" quite literally, these *are* islands, so it makes sense that we would want to implement different types of world generation for your islands!

<details>
  <summary> Sky / Void Generation </summary>
  	The traditional skyblock experience, where your island will be generated in an endless void. Think of how the end islands spawn, out in the vast nothingness.
</details>

<details>
  <summary> Custom Islands </summary>
  We heard you like customization, so we made a crucial decision to allow server owners to set up custom schematics. Game-changing, we know.
  
  Each island in the config has three schematics associated with it, one for each dimension. 
  
  > Note: The schematic file you use changes depending on the version of Minecraft you're using. 
{.is-info}
  
  Schematics are version independent, but newer schematics cannot be used on older versions. If you're using a version below **1.16**, you will likely need to provide a custom schematic.
  
  <details>
    <summary> Show Examples </summary>
    
![custom-classic.png](/custom-classic.png)
> *A custom schematic added to IridiumSkyblock, fashioned after the original Skyblock survival challenge.*
    
![custom-topical.png](/custom-tropical.png)
> *A custom schematic added to IridiumSkyblock, developed and created by community member Hetti. They have a customized configuration for our plugin listed [here](https://builtbybit.com/resources/advanced-iridium-skyblock-config.23789/).*
    
  </details>
  
</details>

<details>
  <summary> Biomes </summary>
  Your super cool ice paradise looks absolutely great, but there's a problem - it keeps melting! Not to worry, you can select the biome that your island spawns with, schematic dependent. This can be used to add a bit of challenge, so use it wisely!
  
  Players can also buy a biome to replace the one their island came with through `/is biomes`.
  </details>
  
<p> &nbsp </p>

# Gameplay

<p> &nbsp </p>

## Leaderboard

IridiumSkyblock comes with a leaderboard included in the plugin, accessible through `/is top`. This menu shows a list of players who are at the top of their game, and you can filter it by either their island's value or their island's level.

<p> &nbsp </p>

### Value

Every island has a value attached to it based on the types of blocks that are placed within its borders. More high-value blocks means a higher value island, and this is reflected in the placeholders.

<p> &nbsp </p>

### Level

An island's level depends on the amount of island experience that it's gathered, which is earned through missions. Higher levels can unlock more missions, and even certain features, like the Nether. This is reflected in the placeholders.

<p> &nbsp </p>

## Economy

The economy has two parts, and using them in tandem will help to create a well-balanced economy.

<details>
    <summary> Vault </summary>
    IridiumSkyblock takes advantage of Vault to hook into any economy that also uses Vault, and by doing so, you can bring your own economy!
  </details>
  
  <details>
    <summary> Crystals </summary>
    Island Crystals are a currency unique to IridiumSkyblock, and they can be used alongside your Vault currency to purchase upgrades, shop items, and more.
  </details>
  
  <details>
    <summary> Bank </summary>  

  Take your crystals with you by depositing them in the Island Bank. This feature allows all members of an island access to a central resevoir of earned income, whether that be currency, crystals, or even experience. The bank is accessible by all players of an island through `/is bank`.
  </details>
  
<p> &nbsp </p>
  
## Shop

The shop is broken up into categories, which are fully configurable, and items, which are also fully configurable. Items can also be purchased with commands attached to them, so if you have a super rare unique item that another plugin has to give your players, you can use its `/give` command or equivalent to make sure that good ends up in your player's lap.

<p> &nbsp </p>

## Missions
  
Missions give players a fun task, and in exchange they receive nifty rewards and Island Experience, which helps to level up their island. You can also reward players for their effort with unique items they otherwise won't come across, such as spawners, end portal frames, spawn eggs, and more. 
  
<p> &nbsp </p>
  
## Co-op

Minecraft is a game about using blocks to make anything you can imagine, and while that's fun to do by yourself, it can get pretty lonely sometimes.

So why not do it with your friends?
  
IridiumSkyblock supports having multiple members of the same island and trusting players to islands without them joining.

<p> &nbsp </p>
  
## Enhancements

One of the things that makes IridiumSkyblock stand out are its enhancements. There are upgrades that players can purchase to upgrade their island and mechanics, and boosters to aid them in accomplishing tasks. Proper configuration of these features can create a fulfilling sense of progression that will keep your players coming back.

<p> &nbsp </p>

### Boosters

Boosters are temporary upgrades for player islands that give specific effects. IridiumSkyblock has a few custom boosters already implemented, and you can set potion effects as boosters, too. You can expand on this with the API.

<p> &nbsp </p>

### Upgrades

Upgrades are permanent upgrades for player islands that give specific effects. IridiumSkyblock has a plethora of custom upgrades already implemented. You can expand on this with the API.
  
<p> &nbsp </p>

## Generators

The cobblestone generator, the trusty, long-standing fluid mechanic that gives players their start in Skyblock. 
  
Humble beginnings, but now with an advanced twist - server owners can set what the generator actually generates. Ever wanted your generator to produce gold instead of cobblestone? Of course you have.
  
The generators can be upgraded, and each level can be modified to produce different blocks.
  
<details>
    <summary> Cobblestone Generator </summary>

To build a cobblestone generator, you will need:
- 1 lava bucket.
- 1 water bucket.
- A 4x3 space.

---

Follow these steps to build a cobblestone generator:
1. Dig out an L-shaped pit in the ground, or build one with available blocks. The L should have two blocks on top, and one block below the second block.
2. Place the water bucket in the first space you made. The water should flow down into the hole.
3. Remove the block directly next to where the water flows and starts its fall. This is where the cobblestone will generate.
4. Remove the next adjacent block, and place the lava there when you're ready. The lava will slowly flow towards the water, and if you did everything correctly, a cobblestone block will generate there instead.
    
    <details>
      <summary> Obsidian In The Generator? </summary>
      
      When the config option "obsidianBucket" is set to true (`obsidianBucket: true` in `configuration.yml`), a player can right-click on a block of obsidian with an empty bucket to return it to its lava state. Great for new players who are learning how to build a cobblestone generator.
      
    </details>

![cobblestone_generator.png](/cobblestone_generator.png)
> *A bisection of a cobblestone generator.*

  </details>
  
  <details>
    <summary> Basalt Generator </summary>
    
To build a basalt generator, you will need:
- 1 lava bucket.
- 1 block of blue ice.
- 1 block of soul soil.
- A 3x3 space.

---

Follow these steps to build a basalt generator:
1. Dig out a spot for the blue ice to be placed.
2. Remove the block next to the blue ice, where you want your basalt to generate.
3. Remove the block below there, and replace it with soul soil.
4. Dig out the block next to where you want your basalt to generate, and place your lava bucket there. If you did everything correctly, the lava will slowly flow over the soul soil, and a basalt block will be generated on top of it.
  
  The basalt generator is unique in the fact that it can be locked into only being usable in the Nether, configurable by enabling `netherOnlyGenerator` in `configuration.yml`.

![basalt_generator.png](/basalt_generator.png)
> *A bisection of a basalt generator.*
    
  </details>
  
<p> &nbsp </p>
  
## Restarting

Players can reset their island without deleting them. By using `/is regen`, they can pick what schematic they would like, and the plugin will refresh their space with that schematic. You can configure this to wipe island data, as well.

Servers can charge players for regenerating their islands, with prices changing depending on the schematic selected, if desired.

<p> &nbsp </p>

# Server

<p> &nbsp </p>

## Placeholders
  
IridiumSkyblock comes with a plethora of placeholders to populate your play tables.
Supports Placeholder API.
  
Read more on our [Placeholders](https://docs.iridiumdevelopment.net/en/Placeholders) page.

<p> &nbsp </p>

## Commands

All the commands added through the plugin are configurable, and you can set an alias, permissions, and even toggle whether they're enabled on your server.
  
Read more on our [Commands](https://docs.iridiumdevelopment.net/en/Commands) page.



