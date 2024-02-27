---
title: Frequently Asked Questions
description: A list of frequently asked questions for you to search, in case you need help.
published: true
date: 2023-09-29T14:46:31.729Z
tags: 
editor: undefined
dateCreated: 2023-08-06T21:53:24.551Z
---

# Frequently Asked Questions

> Note: If you have a question that isn't on this page, feel free to ask us in our [Discord](https://discord.com/invite/6HJ73mWE7P) server!
> (Read the rules first, though.)
{.is-info}

> Note: Listed yaml configuration has been truncated for demonstration purposes. Please do not directly copy/paste into your own configuration.
{.is-warning}

To search this FAQ quickly, we recommend using your browser's search function (ctrl + F / command + F).

<p> &nbsp </p>
 
## Will my data reset between V3 and V4?

Yes.

Technically speaking, your configurations will be reset, as the plugin will no longer recognize them as valid. The physical islands will still be present in the world, but because there is a discrepancy in how the database is written between V3 and V4, the plugin will not recognize that they belong to anyone.
 
### What about between V4 versions?
No, versions that begin with a **4** are fully compatible with each other.
 
### Is there going to be a data transfer tool for V3 -> V4?
"No" - Making a data converter is complicated, and this would take away from the focus on making IridiumSkyblock a better plugin. There is still the possibility of one, but don't count on it.

<p> &nbsp </p>

## What is IridiumTeams?

IridiumTeams is the parent plugin of IridiumSkyblock and IridiumTowns.

In essence, it allows us to create a more cohesive development experience, as we can unify the code that creates the islands and other common features and work on them separately from the plugin, should the need arise.
 
### What is IridiumCore?
IridiumCore is the library that most of Iridium Development's plugins use. It makes it easier to work on plugin updates for new Minecraft releases and houses most of the groundwork for the plugin to function.

<p> &nbsp </p>

## The plugin isn't working!

Make sure you have Vault installed, and that you're running a compatible version of Minecraft and Spigot or one of its forks.
See [here](https://docs.iridiumdevelopment.net/en/Installation).
 
### I have Vault, and the plugin still isn't loading.
Check your server's console/log, there is probably an error that explains the issue.
 
### The plugin stopped working!
This is most likely a result of "hot-loading" the configuration. 
By using the `/is reload` command, you can change the configuration of the plugin while it's currently running. However, if your configuration has a syntax issue or invalid value, the plugin will disable itself to prevent issues, and an error in the console/log will describe the problem.

<p> &nbsp </p>

## How do I give players money?

`/is bank give <CURRENCY> <PLAYER>`

Accepted Currency: `money`, `Crystals`, `experience`, and custom bank items.

<p> &nbsp </p>
  
## How do I disable a feature?

Most features can be disabled by disabling their associated command.
You can do this by changing `enabled` to `false` in `commands.yml`.

```yaml
commandName:
  enabled: false
```
 
### What if the feeature I want to disable doesn't have a command?

You'll find the ability to disable it in the same place you can configure it. For upgrades, like the cobblestone generator, you can do this in enhancements.yml.
 
### The feature I disabled is still listed in the plugin menu.

You'll need to remove it from inventories.yml.

```yaml
feature:
    slot: null
```

<p> &nbsp </p>

## How do I increase or decrease the distance between islands?

You can change the distance between player islands by changing `distance` in `configuration.yml`.

```yaml
distance: 151
```
  
**Do _NOT_ change this value while existing player islands are established**, or they will lose their islands. This occurs because the plugin moves the borders and not the actual blocks. If you want to move the borders anyway, you can manually copy/paste their islands using a tool like World Edit.
 
### What about increasing or decreasing island sizes?

You can change the size of player islands by changing the size value under the level of the upgrade you're trying to change in `enhancements.yml`.

```yaml
sizeEnhancement:
  levels:
    0:
      size: 50
```

If you want players to have a fixed island size, you can delete the other enhancement levels and change the size at level 0.
  
<p> &nbsp </p>  
  
## How do I change the command prefix?

This isn't something you can do in our configuration. Instead, you need to change `plugin.yml`, which is a file in our source code.

Not to worry, this is very easy!

```yaml
commands:
  iridiumskyblock:
    aliases: [ "island", is ]
```
  
Once you've changed the command prefix to what you want it to be, you need to compile the plugin.

`gradle build`

The compiled `.jar` file will be found in `IridiumSkyblock/build/libs`.

<p> &nbsp </p>
  
## How do I change where rewards are sent?

All mission rewards must be redeemed through `/is rewards`. However, you can change where these rewards go, as well as what is being rewarded.
  
```yaml
reward:
  money: 1000.0         (Player)
  bankRewards:
    money: 10.0         (Bank)
    Crystals: 5.0       (Bank)
    experience: 15      (Bank)
  experience: 0         (Player)
  teamExperience: 10    (Island)
```
  
All values under `bankRewards` are sent to the player's Island Bank, whereas all values outside of this are sent directly to the player, with the exclusion of `teamExperience`, which is Island Experience and is not redeemable for player experience.
 
### Can I change the level scaling for missions?

Not in the configuration. You'll need to edit the source code.
  
<p> &nbsp </p>
  
## How do I change the starter island?

You'll need to replace the island's schematic with your own, or add your own schematic to the plugin.
See [here](https://docs.iridiumdevelopment.net/en/Schematics).
 
### How do I change the contents of the chest?

You'll need to change the schematic. Load the schematic using a plugin like World Edit, change the contents of the chest, and then save it again, and make sure that any changes made to the name are reflected in `schematics.yml`.

<p> &nbsp </p>
  
## How do I delete a player's inventory when they regenerate/delete their island?

If you enable `clearInventoryOnRegen` and `clearEnderChestOnRegen` in `configuration.yml`, when a player regenerates or deletes their island, every player that belongs to that island will have their inventory and/or enderchest deleted.
  
<p> &nbsp </p>  
  
## How do I remove the Patreon message?

This message is only sent to players with admin privileges, such as opped players. If you would like to disable it, you can change `patreonMessage` to false in `configuration.yml`.
  
<p> &nbsp </p>  
  
## Do you have a PAPI eCloud extension?

No.

Back on V2, a third party had made a PAPI eCloud extension to use with our plugin. This extension will break newer versions of IridiumSkyblock's placeholders, and while we had reached out to the team behind the eCloud to get it taken down, they did not remove it. 

We apologize for the confusion.
 
### My placeholders aren't working!

If you're using the correct placeholders, make sure that you have Placeholder API (PAPI) installed.
See [here](https://docs.iridiumdevelopment.net/en/Placeholders).
  
<p> &nbsp </p>
  
## Can I split IridiumSkyblock across multiple worlds/servers?
  
No.

Every island will be on the same world, and IridiumSkyblock will only govern the three worlds it creates. However, if you plan to host Skyblock as a gamemode on your network, IridiumSkyblock will work out of the box as its own standalone server.

<p> &nbsp </p>  
  
## Why is my island generating in a normal world?
  
You either loaded the world while IridiumSkyblock was disabled, or there was an error loading the chunk generator.
The only way to fix this is to clear the generated chunks with a plugin like World Edit and ensure that the world is only loaded when IridiumSkyblock is enabled with a working chunk generator.

We recommend that servers download a plugin like VoidGen and use a plugin like Multiverse to set the world's generator to the one provided by VoidGen. This way, if the world is ever loaded and IridiumSkyblock is disabled, the chunks that are generated are empty.
 
### Why do islands stick around after players delete them?
  
You may notice that islands are not fully deleted when a player deletes their island. You can change `removeIslandBlocksOnDelete` to true in `configuration.yml` to change this behavior and delete the island when a player deletes it.
  
<p> &nbsp </p>
  
## Do you offer checksums for your plugin?
  
"Yes".

As part of our development cycle, we have an automated pipeline that submits successful builds of IridiumSkyblock to our Nexus repository. Nexus is also where the automated pipeline places checksums for the generated builds, so if you want to cross-reference checksums, you will need to find the correct version of the plugin you're downloading here and compare the generated checksum.
  
<p> &nbsp </p>
  
## How do I keep my Survival and Skyblock modes separated?
  
The responsible way to separate Survival and Skyblock gamemodes would be to host two different servers and connect them through a proxy, like Bungeecord or Velocity. That way, everything stays totally separate, and players can travel between the two (or more) servers freely by using `/server <SERVER>`. This also keeps exploits to a minimum and allows administrators finer control over their network.
 
### I don't want to / I can't do this with my current host.
  
You can use a per-world plugin limiter to separate the plugins by world. We can't guarantee the results of using this method, though, so if you encounter issues this way, we won't be able to provide support.

<p> &nbsp </p>
  
## How do I edit the ore generator?
  
The ore generator provided by the plugin works in the same way a raffle does - every item listed has an equal chance to be pulled, but items with a higher value have a higher chance of being successfully pulled because they have multiple entries.
  
```yaml
generatorEnhancement:
  levels:
    0:
      ores:
        COBBLESTONE: 3
        COAL_ORE: 1
      netherOres:
        BASALT: 1
```
  
In this example, the cobblestone generator has a 3/4 chance to generate Cobblestone, and a 1/4 chance to generate Coal Ore; while there are only 2 block types listed, there are a total of 4 entries.

Similarly, the basalt generator has a 1/1 chance to generate basalt, meaning that the basalt generator at this level will only generate basalt, because that is the only entry it can roll for.
 
### Can I make the generator work in percentages instead?
  
If you make the sum of all items on the table equal to 100, then it will be the same as the generator working in percentages.
  
```yaml
levels:
    0:
      ores:
        COBBLESTONE: 75
        COAL_ORE: 25
      netherOres:
        BASALT: 100
```
  
With this configuration, there is a 75% chance of Cobblestone generating, and a 25% of Coal Ore generating in the cobblestone generator, for a total of 100%. In the basalt generator, basalt has a 100% chance of spawning.
  
<p> &nbsp </p>
  
## How do I disable the Nether and End?
  
The Nether and End are enabled by default, but you can disable them by changing the following settings in `configuration.yml`.
  
```yaml
enabledWorlds:
  NORMAL: true
  NETHER: false
  THE_END: false
```
  
<p> &nbsp </p>
  
## I think I found a bug!
  
A bug in IridiumSkyblock can happen sometimes, and that's okay! Make sure that the issue you're experiencing is a result purely from IridiumSkyblock by replicating the issue on a test server with only IridiumSkyblock, Vault, an economy, and Placeholder API (if you think this is a plugin conflict that should not exist, include the conflicting plugin). If you can successfully replicate, make a bug report on our [Issues](https://github.com/Iridium-Development/IridiumSkyblock/issues) page, and please follow our reporting guidelines!