---
title: Commands & Permissions
description: This page details how to configure the commands provided with the plugin, including their associated permissions.
published: true
date: 2023-09-29T16:46:27.427Z
tags: 
editor: undefined
dateCreated: 2023-08-06T23:26:27.431Z
---

> Iridium Development does not condone the usage of permissions for locking features or content behind paywalls, premium ranks, or predatory behavior (Pay To Win, or P2W). Please make sure that your server is in compliance with both the [Minecraft EULA](https://www.minecraft.net/en-us/eula) and the [Minecraft Usage Guidelines](https://www.minecraft.net/en-us/usage-guidelines), in which your server is specifically eligible for (regardless of the server software you use): 
> 
> As of September 29th, 2023;
> 
> - "Selling entitlements that affect gameplay provided they don’t ruin other players’ experience or give a competitive advantage in the game."
>
> - "Asking for donations, so long as you don’t offer the donor something that only they can use. However, you may offer all players server wide rewards if donation goals are met."
>
> If you are unsure of what your rights are as a server owner, please contact a lawyer for legal counseling.
{.is-warning}

# Required Reading

IridiumSkyblock handles permissions in a different way compared to most other plugins on the market. Instead of registering all available permissions with a permission plugin, we check the configuration of `commands.yml` for permissions listed and cross-check our commands with them before executing. This approach allows us to have a more flexible permissions system.

This document will outline the basics of this unique approach, and define what commands have more explicit permissions.

<p> &nbsp </p>

# Configuration

Every command in IridiumSkyblock has configuration that is outlined in your `commands.yml` file.

---
```yaml
bankCommand:
  aliases:
  - "bank"
  description: "View your Island bank"
  syntax: "%prefix% &7/is bank <give/set/remove> <player> <item> <amount>"
  permission: ""
  cooldownInSeconds: 0
  enabled: true
  adminPermission: "iridiumskyblock.bank.modify"
```
> *The default configuration for `/is bank`.*
---

- **Command**: the command category in which the other configuration options reside.
	- *aliases*: ^[String]^ Allows you to define command aliases.
	- *description*: ^[String]^ The description that appears in ``/is help``
	- *syntax*: ^[String]^ Shows players how to use the command.
	- *permission*: ^[String]^ The permission required to run this command.
  - *cooldownInSeconds*: ^[int]^ The amount of time in seconds before a user can run this command again.
  - *enabled*: ^[boolean]^ Whether the command is enabled for your server.
  - *adminPermission*: ^[String]^ The permission required to run this command as an administrator.

<p> &nbsp </p>

# Commands

Servers will need to use their permissions plugin to assign players their permissions. This is done in the same manner as permissions from another plugin, but they will not be listed under a drop-down or under the plugin's permissions, with the occasional exception of admin permissions.

> Note: We recommend using [LuckPerms](https://luckperms.net/).
{.is-info}

> Note: Commands have server-defined permissions. Any permissions you see listed on this page are default permissions and are not necessarily the permissions outlined by your configuration. Please see the above section on configuration for more information.
{.is-info}

<details>
  <summary> Example </summary>
  

`/lp user <PLAYER> permission set iridiumskyblock.bypass true`

This command will give the specified player the `iridiumskyblock.bypass` permission using LuckPerms.

</details>

<p> &nbsp </p>
  
## Player Commands

### Gameplay Commands

<details>
  <summary> Show Table </summary>
  
|Command|Shortcut|Description|Syntax|
|-------|--------|-----------|------|
|about  |...|Shows information about the plugin.|`/is about`|
|bank   |...|Brings up the island bank.|`/is bank`|
|boosters|...| Brings up the Booster menu.|`/is boosters`|
|border|...|Brings up the Border menu and allows players to change the color or toggle with the command.|`/is border <COLOR>`|
|create|...|Brings up the Island Creation menu.|`/is create`|
|delete|...|Deletes a player's island (Brings up a confirmation screen).|`/is delete`|
|deletewarp|delwarp|Delete's an island warp (Brings up a confirmation screen).|`/is deletewarp <WARP>`|
|deposit|...|Deposits currency or experience into the bank.|`/is deposit <TYPE> <AMOUNT>`|
|description|...|Changes the description of a player's island.|`/is description <DESCRIPTION>`|
|editwarp|...|Edits an existing warp using a command.|`/is editwarp <WARP> <ICON/DESCRIPTION> <VALUE>`|
|fly|...|Toggles the fly booster.|`/is fly <ON/OFF/ENABLE/DISABLE>`|
|help|...|Shows a list of commands.|`/is help`|
|home|...|Sends the player to their island.|`/is home`|
|info|...|Shows information about the current island.|`/is info`|
|level|...|Shows the current Island level.|`/is level`|
|missions|...|Displays the Missions menu.|`/is missions <TYPE>`|
|regen|...|Regenerates a player's island.|`/is regen <SCHEMATIC>`|
|rename|...|Renames a player's island.|`/is rename <NAME>`|
|rewards|...|Brings up the Rewards menu.|`/is rewards`|
|sethome|...|Changes the location of the Island home.|`/is sethome`|
|settings|...|Brings up the Island Settings menu.|`/is settings`|
|setwarp|...|Creates an island warp.|`/is setwarp`|
|shop|...|Brings up the Island Shop.|`/is shop`|
|top|...|Brings up the Top Islands menu.|`/is top`|
|transfer|...|Allows a player to transfer their island to another player.|`/is transfer <PLAYER>`|
|upgrades|...|Brings up the Upgrades menu.|`/is upgrades`|
|value|...|Shows the current Island value.|`/is value`|
|warp|...|Warps a player to the specified warp.|`/is warp <WARP>`|
|warps|...|Brings up the Island Warps menu.|`/is warps`|
|withdraw|...|Withdraws currency or experience from the Island Bank.|`/is withdraw <TYPE> <AMOUNT>`|

</details>

<p> &nbsp </p>
  
### Co-op
  
<details>
  <summary> Show Table </summary>
  
|Command|Shortcut|Description|Syntax|
|-------|--------|-----------|------|
|chat|c|Allows players to switch between using Island Chat or Global Chat.|`/is chat <TYPE>`|
|demote|...|Demotes an Island Member to the previous rank.|`/is demote <PLAYER>`|
|invite|...|Invites a player to your island.|`/is invite <PLAYER>`|
|invites|...|Shows currently available invites to other players islands.|`/is invites`|
|join|...|Asks another player to join their island.|`/is join <PLAYER>`|
|kick|...|Kicks a player from the island.|`/is kick <PLAYER>`|
|leave|...|Removes the player from the island
|members|...|Brings up the Island Members menu.|`/is members`|
|permissions|...|Brings up the Island Permissions menu.|`/is permissions`|
|promote|...|Promotes an Island Member to the next rank.|`/is promote <PLAYER>`|
|setpermission|...|Sets what permissions each rank of an island has.|`/is setpermission <PERMISSION> <RANK> <TRUE/FALSE>`|
|top|...|Brungs up the Top Islands menu.|`/is top`|
|transfer|...|Transfers island ownership to another player.|`/is transfer`|
|trust|...|Trusts a player to your island with Member permissions.|`/is trust <PLAYER>`|
|trusts|...|Shows a list of trusted players.|`/is trusts`|
|uninvite|...|Revokes an invite from a player.|`/is uninvite <PLAYER>`|
|untrust|...|Revokes trust from a player.|`/is untrust <PLAYER>`|
|visit|...|Visits another player's island.|`/is visit <PLAYER>`|
  
</details>
    
<p> &nbsp </p>
  
## Administration Commands
  
<details>
  <summary> Show Table </summary>
    
|Command|Shortcut|Description|Permission Required|Syntax|
|-------|--------|-----------|-------------------|------|
|bank   |...|Brings up the island bank.|`iridiumskyblock.bank.modify`|`/is bank`|
|delete|...|Deletes a player's island (Brings up a confirmation screen).|`iridiumskyblock.delete.others`|`/is delete <ISLAND>`|
|description|...|Changes the description of a player's island.|`iridiumskyblock.description.others`|`/is description <ISLAND> <DESCRIPTION>`|
|experience|...|Changes the amount of experience the current island has.|`iridiumskyblock.experience.modify`|`/is experience <GIVE/SET/REMOVE> <PLAYER> <AMOUNT>`|
|recalculate|recalc|Performs recalculation of all island statistics.|`iridiumskyblock.recalculate`|`/is recalculate`|
|reload|...|Reloads the IridiumSkyblock config.|`iridiumskyblock.reload`|`/is reload`|
|rename|...|Renames a player's island.|`iridiumskyblock.rename.others`|`/is rename <NAME>`|
    
</details>