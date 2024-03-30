---
title: Placeholders
description: A list of all of IridiumSkyblock's placeholders.
published: true
date: 2024-03-30T20:23:28.838Z
tags: 
editor: markdown
dateCreated: 2024-02-27T19:05:07.463Z
---

<center>

<body>
  <div class="placeholderBuilder">
    Placeholder Builder Tool
    <div class="placeholderSelection">
      <div class="select">
					<select class="select-text" id="prefix" required onchange=changePrefix(this)>
						<option value="" disabled selected></option>
            <optgroup label="Prefixes">
            <option value="island">island</option>
            <option value="current_island">current_island</option>
            <option value="top_value_#_island">top_value_#_island</option>
            <option value="top_experience_#_island">top_experience_#_island</option>
            </optgroup>
					</select>
					<span class="select-highlight"></span>
					<span class="select-bar"></span>
					<label class="select-label">Select Prefix</label>
				</div>
      <div class="select">
					<select class="select-text" id="body" onchange=changeBody(this) required>
						<option value="" disabled selected></option>
            <optgroup label="Player Placeholders">
            <option value="player_rank">player_rank</option>
            <option value="player_name">player_name</option>
            <option value="player_join">player_join</option>
            </optgroup>
            <optgroup label="Skyblock Placeholders">
            <option value="name">name</option>
            <option value="owner">owner</option>
            <option value="description">description</option>
            <option value="create">create</option>
            <option value="value">value</option>
            <option value="level">level</option>
            <option value="experience">experience</option>
            <option value="value_rank">value_rank</option>
            <option value="experience_rank">experience_rank</option>
            <option value="members_online">members_online</option>
            <option value="members_online_count">members_online_count</option>
            <option value="members_offline">members_offline</option>
            <option value="members_offline_count">members_offline_count</option>
            <option value="members_count">members_count</option>
            <option value="bank_<TYPE>">bank</option>
            <option value="<MATERIAL>_amount">block_amount</option>
            <option value="<ENTITY>_amount">entity_amount</option>
            </optgroup>
					</select>
					<span class="select-highlight"></span>
					<span class="select-bar"></span>
					<label class="select-label">Select Body</label>
		</div>
  </div>
</div>
  <div id="builder">
      <span>%iridiumSkyblock_</span>
      <span id="prefix_display">p</span>
      <span>_</span>
      <span id="body_display">b</span>
      <span>%</span>
    </div>
</body>
 
<script>
  function changePrefix(prefixSelector) {
    var prefix = prefixSelector.value;
    if(prefix == "") {
    	document.getElementById("prefix_display").style.visibility= "hidden";
      return;
    }
    document.getElementById("prefix_display").innerHTML = prefix;
  }
</script>

<style>
  
  .builder {
    display: flex;
    flex-direction: row;
  }
  
  .placeholderBuilder {
    background-color: #176CC8;
    border: 5px solid rgba(23, 108, 200, 0.5);
    -webkit-background-clip: padding-box;
  	display: flex;
    flex-direction: column;
    padding: 20px;
    height: 200px;
    margin: 20px;
    justify-content: space-evenly;
  }
  
  .placeholderSelection {
      display: flex;
      flex-direction: row;
      padding: 5px;
      justify-content: space-evenly;
    	align-items: center;
  }
  
  .body {
  position: relative;
  font-family:
    'Roboto','Helvetica','Arial',sans-serif;
  }

  .wrap {
    position: absolute;
    right: 0;
    top: 40%;
    width: 350px;
    left: 0;
    margin: 0 auto;
  }
  
  .select {
    font-family:
      'Roboto','Helvetica','Arial',sans-serif;
	  position: relative;
	  width: 350px;
    margin: 0 auto;
  }

  .select-text {
	  position: relative;
	  font-family: inherit;
    color: #000000 !important;
	  background-color: transparent;
	  width: 350px;
	  padding: 10px 10px 10px 0;
	  font-size: 18px;
	  border-radius: 0;
	  border: none;
	  border-bottom: 1px solid rgba(255,255,255, 0.65);
  }

  .select-text:focus {
	  outline: none;
	  border-bottom: 1px solid rgba(255, 255, 255, 0.10);
  }

  .select .select-text {
	  appearance: none;
	  -webkit-appearance:none
}

  .select:after {
	  position: absolute;
	  top: 18px;
	  right: 10px;
	
	  width: 0;
	  height: 0;
	  padding: 0;
	  content: '';
	  border-left: 6px solid transparent;
	  border-right: 6px solid transparent;
	  border-top: 6px solid rgba(255, 255, 255, 0.65);
	  pointer-events: none;
}
  
  .select-label {
	  color: rgba(255,255,255, 0.65);
	  font-size: 18px;
	  font-weight: normal;
	  position: absolute;
	  pointer-events: none;
	  left: 0;
	  top: 10px;
	  transition: 0.2s ease all;
  }

  .select-text:focus ~ .select-label, .select-text:valid ~ .select-label {
	  color: #81A9FF;
	  top: -20px;
	  transition: 0.2s ease all;
	  font-size: 14px;
  }

  .select-bar {
	  position: relative;
	  display: block;
	  width: 350px;
  }

  .select-bar:before, .select-bar:after {
	  content: '';
	  height: 2px;
	  width: 0;
	  bottom: 1px;
	  position: absolute;
	  background: #2F80ED;
	  transition: 0.2s ease all;
  }

  .select-bar:before {
	  left: 50%;
  }

  .select-bar:after {
	  right: 50%;
  }

  .select-text:focus ~ .select-bar:before, .select-text:focus ~ .select-bar:after {
	  width: 50%;
  }

  .select-highlight {
	  position: absolute;
	  height: 60%;
	  width: 100px;
	  top: 25%;
	  left: 0;
	  pointer-events: none;
	  opacity: 0.5;
  }
</style>
  
</center>

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