---
title: Unsupported Content
description: A list of known incompatibilities with IridiumSkyblock.
published: true
date: 2023-08-12T12:40:31.871Z
tags: 
editor: undefined
dateCreated: 2023-08-07T20:25:33.083Z
---

The goal of this page is to serve as a warning to future server owners as to what plugins we know don't work well with IrdiumSkyblock and to document known incompatibilities we can't fix.

# Server

<p> &nbsp </p>

## Versions below 1.13

These versions of Minecraft run on a vastly different system compared to versions **1.13** and after, and thus are not compatible with IridiumSkyblock. You can read about [The Flattening](https://minecraft.fandom.com/wiki/Java_Edition_1.13/Flattening) here.

<p> &nbsp </p>

## Vanilla Server / Craftbukkit

Servers need to be running at least Spigot. The plugin relies on code that is not in Vanilla or Craftbukkit.

<p> &nbsp </p>

## Missing Vault

The plugin requires Vault to function. See our [Installation guide](https://docs.iridiumdevelopment.net/en/Installation) for more information.

<p> &nbsp </p>

# Plugins

<p> &nbsp </p>

## PlugMan / PlugMan X
PlugMan forces the plugin to shutdown, and then re-enables it through the Bukkit API, which causes problems with the way that IridiumSkyblock will load. This causes many problems, and as such we cannot support servers that use PlugMan.


<p> &nbsp </p>

## CMI Economy
CMI Economy uses an unconventional Vault hook that can cause duplication and other glitches with the currency count.


<p> &nbsp </p>

## Multiverse Nether Portals
IridiumSkyblock purposefully ignores the 1/8th scaling that the Minecraft Nether has in order to respect island sizes and locations. As a result, Multiverse Nether Portals will not place portals in the correct locations, which can cause problems with portal linking.


<p> &nbsp </p>

## Geyser
While the plugin itself loads fine on servers with Geyser installed, Bedrock players will have difficulty navigating the menus. This is a limitation of Geyser.



<p> &nbsp </p>

## Slimeworld / MyWorld
IridiumSkyblock does not currently support these formats.


<p> &nbsp </p>