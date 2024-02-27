---
title: Installation
description: Getting Started with IridiumSkyblock
published: true
date: 2024-02-18T15:15:45.649Z
tags: 
editor: markdown
dateCreated: 2023-03-29T15:34:46.219Z
---

# Requirements

IridiumSkyblock requires the following to load:

- [Spigot](https://www.spigotmc.org/), or one of its forks, for Minecraft version **1.13** or later.
- [Vault](https://www.spigotmc.org/resources/vault.34315/).

<p> &nbsp </p>

## Recommendations

While these plugins are not mandatory for IridiumSkyblock to load, they add functionality that is considered essential on most servers.

- A Spawn Plugin (For providing a way to return to the default world).
- An Economy Plugin that supports Vault (Required for any currency to be used or rewarded).
- [Placeholder API (PAPI)](https://www.spigotmc.org/resources/placeholderapi.6245/) (For placeholders to function across other plugins).
- [World Edit](https://enginehub.org/worldedit) (For making schematics).

<p> &nbsp </p>

> We recommend using **1.16+**, as previous versions have performance issues and lack features. We also recommend using [Paper](https://papermc.io/) or [Purpur](https://purpurmc.org/).
>
> If you are not running a version listed above, either update your server or do not use IridiumSkyblock, as it will not work properly.
{.is-info}

> Note: IridiumSkyblock currently does **NOT** support [Folia](https://github.com/PaperMC/Folia). It will not load on any server using this software.
{.is-warning}

<p> &nbsp </p>

# **Installation Steps**

1. Download the plugin from [Spigot](https://www.spigotmc.org/resources/iridium-skyblock-1-13-1-19.62480/) or [Modrinth](https://modrinth.com/plugin/iridiumskyblock).
2. Place the downloaded file in your `server/plugins` folder.
3. Restart your server by running `stop` in the console and allowing the server to fully shutdown, then start the server again.

>  [Do **NOT** use the `/reload` command](https://madelinemiller.dev/blog/problem-with-reload/), or any plugin that reloads your server or plugins, like PlugManX. This breaks the way that IridiumSkyblock (and many other plugins) functions, and can cause data loss. You will not receive support for this plugin if you are using these methods.
{.is-danger}

> After that, IridiumSkyblock should populate your `server/plugins/IridiumSkyblock` folder with all the files it needs to work properly.
{.is-success}

<p> &nbsp </p>

You should see the following in `plugins/IridiumSkyblock`:

<details>
  <summary>Config files (.yml)</summary>
  
  - `bankitems.yml`
  - `biomes.yml`
  - `blockvalues.yml`
  - `commands.yml`
  - `configuration.yml`
  - `enhancements.yml`
  - `inventories.yml`
  - `messages.yml`
  - `missions.yml`
  - `permissions.yml`
  - `schematics.yml`
  - `settings.yml`
  - `shop.yml`
  - `sql.yml`
  - `top.yml`
  
</details>
 
<details>
 <summary>Database file (.db)</summary>
 
   - `IridiumSkyblock.db`
</details>
  
<details>
  <summary> Schematic files (.schem) </summary>

  - `IridiumSkyblock/schematics`
    - `desert.schem`
    - `desert_end.schem`
    - `desert_nether.schem`
    - `jungle.schem`
    - `jungle_end.schem`
    - `jungle_nether.schem`
    - `mushroom.schem`
    - `mushroom_end.schem`
    - `mushroom_nether.schem`
</details>

You can also confirm that IridiumSkyblock loaded by running `/is about` or by searching your console log for the message that IridiumSkyblock sends when it's enabled.

---
![A screenshot of the `/is about` command.](/screenshot_2023-03-29_224920.png)
>*A screenshot of the `/is about` command. Your message may have a different version listed.*
---

As you can see in the example image, IridiumSkyblock has loaded and is working properly.

<p> &nbsp </p>

If you do not see this, but instead an error or unknown command prompt, please make sure that you have Vault installed, and that you're running a supported version of Minecraft and Spigot (or its forks). The plugin will either show up in red when using `/plugins` (`/pl`) or it will not show up at all, and there will be an error in the console explaining the problem.

Example: 

> [19:36:49 ERROR]:  Could not load 'plugins\IridiumSkyblock-4.0.jar' in 'plugins'
>
> org.bukkit.plugin.UnknownDependencyException: Unknown/missing dependency plugins: [Vault]. Please download and install these plugins to run 'IridiumSkyblock'.
{.is-danger}

If you see this error, that means that you do not have Vault installed. Please download and install Vault to run IridiumSkyblock.

<p> &nbsp </p>

# Supported Plugins / Extra Features

These plugins are supported by IridiumSkyblock, and installing them will provide your server with extra features not otherwise implemented into the main plugin.

Please note that IridiumDevelopment will not be able to provide support for plugins outside the IridiumDevelopment family, but we're more than happy to try and point you in the right direction. 

You should probably ask for support from the developers.

<p> &nbsp </p>

## Supported Plugins

<details>
  <summary> World / Schematic Generation </summary>
  
- [World Edit](https://enginehub.org/worldedit)
- [Fast Async World Edit (FAWE)](https://intellectualsites.github.io/download/fawe.html)
  
</details>

<details>
  <summary> Placeholders </summary>
 
- [Placeholder API](https://www.spigotmc.org/resources/placeholderapi.6245/)

</details>

<details>
  <summary> Spawners / Stackers </summary>
  
- [RoseStacker](https://www.spigotmc.org/resources/rosestacker.82729/)
- [WildStacker](https://bg-software.com/wildstacker/)
  
</details>

<details>
  <summary> Economy </summary>
  
  You can use any economy plugin that hooks into Vault, but we recommend one of these.
- [EssentialsX](https://essentialsx.net/)
</details>

<details>
  <summary> Other </summary>
		Placeholder Text
  </details>

> Note: If you'd like to see your plugin listed here, let us know in our [Discord](https://discord.gg/6mdyZbuSDk) server!
> (Read the rules first, though.)
{.is-info}

<p> &nbsp </p>

# Uninstall

In order to properly uninstall IridiumSkyblock from your server, follow these steps.
1. Stop the server.
2. Delete the `plugins/IridiumSkyblock` folder.
3. Delete the `IridiumSkyblock` world folder.
4. Delete the plugin file from `plugins`.
5. Start the server.