---
title: Placeholders
description: A list of all of IridiumSkyblock's placeholders.
published: true
date: 2023-08-09T16:50:51.429Z
tags: 
editor: undefined
dateCreated: 2023-08-07T22:41:36.642Z
---

# Required Reading

IridiumSkyblock placeholders are composed of two components - the **prefix**, which determines what sort of data you're looking for, and the **body**, which determines what value you're looking for.

A placeholder will look like this:

`iridiumskyblock_prefix_body`

<details>
  <summary> Examples </summary>
  
`iridiumskyblock_island_level` 
  
- will display the island level of the player's island.
  <p> &nbsp </p>
  
`iridiumskyblock_top_value_2_island_owner`
  
- will display the username of the player that owns the island with the 2nd highest value.
  <p> &nbsp </p>

`iridiumskyblock_current_island_bank_crystals`
  
- will display the amount of Island Crystals that are in the bank of the island that the player is currently standing on.
  
</details>

> Note: Every placeholder starts with `iridiumskyblock_`.
{.is-info}

# Placeholders

In order to take advantage of these placeholders, please make sure you have both a placeholder API and are using these placeholders with a plugin that has support for it.

<p> &nbsp </p>

## Prefixes

<p> &nbsp </p>

### - `island_`

This will show a value related to the player's island.

---

### - `current_island_`

This will show a value related to the island that the player is currently standing on.

---

### - `top_value_#_island_`

This will show a value related to the island with the # highest block value.

---

### - `top_experience_#_island_`

This will show a value related to the island with the # highest amount of experience.

<p> &nbsp </p>

## Bodies

<p> &nbsp </p>

### Player Placeholders
  
|Body|Description|
|----|-----------|
|`player_rank`|Displays the member rank of the player.|
|`player_name`|Displays the player's name.|
|`player_join`|Displays when the player joined the island.|

<p> &nbsp </p>

### Skyblock Placeholders

|Body|Description|
|----|-----------|
|`name`|Displays the name of the island.|
|`owner`|Displays the username of the island owner.|
|`description`|Displays the description of the island.|
|`create`|Displays when the island was created.|
|`value`|Displays the island's value.|
|`level`|Displays the island's level.|
|`experience`|Displays the amount of experience the island has.|
|`value_rank`|Displays the value rank of the island according to the leaderboard.|
|`experience_rank`|Displays the experience rank of the island according to the leaderboard.|
|`members_online`|Displays currently online members of the island.|
|`members_online_count`|Displays how many members of the island are online.|
|`members_offline`|Displays all members of the island.|
|`members_offline_count`|Displays how many members of the island are offline.|
|`members_count`|Displays how many members the island has.|
|`bank_<TYPE>`|Displays how much of the specified currency or experience is in the bank.|
|`<MATERIAL>_amount`|Displays how many of the specified block are on the island.|
|`<ENTITY>_amount`|Displays how many of the specified entity are on the island.|