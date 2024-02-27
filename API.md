---
title: API
description: Documentation on the API and repo.
published: true
date: 2023-12-19T16:08:27.624Z
tags: 
editor: markdown
dateCreated: 2023-08-07T19:45:11.955Z
---

# Repo

Depending on your build environment, you may need to use different formatting for your build files. Below you'll find formatting for Apache Maven and Gradle (Kotlin DSL).

<details>
  <summary> Apache Maven </summary>

Insert these into your `pom.xml` file.

```xml
<repository>
    <id>iridiumdevelopment</id>
    <url>https://nexus.iridiumdevelopment.net/repository/maven-releases/</url>
</repository>
```
```xml
<dependency>
  <groupId>com.iridium</groupId>
  <artifactId>IridiumSkyblock</artifactId>
  <version>LATEST</version>
</dependency>
```  
  
After that, run `mvn package`, and maven should recognize the dependency and build your project.

</details>

<details>
  <summary> Gradle Kotlin DSL </summary>

Insert these into your `build.gradle.kts` file.

```kts
repositories {
  maven("https://nexus.iridiumdevelopment.net/repository/maven-releases/")
}
```
```kts
dependencies {
  implementation("com.iridium:IridiumSkyblock:LATEST")
}
```

After that, run `gradle build`, and gradle should recognize the dependency and build your project.

</details>

> Note: You may have to change the version that you're compiling against. Change `LATEST` to the version you need.
{.is-info}

---
 
<p> &nbsp </p>

# API (FAQ)

<p> &nbsp </p>
 
## How do I get a Players Island?

First get the User object using the following code.
And then you can retrieve an Optional Island from the user object
```java
public Optional<Island> getPlayerIsland(Player player) {
    User user = IridiumSkyblockAPI.getInstance().getUser(player);
    Optional<Island> island = user.getIsland();
    return island;
}
```

<p> &nbsp </p>
 
## How do I get the Island the Player is currently standing on?

First get the User object using the following code.
And then you can retrieve an Optional Island from the user object
```java
public Optional<Island> getPlayerIsland(Player player) {
    User user = IridiumSkyblockAPI.getInstance().getUser(player);
    Optional<Island> island = user.getCurrentIsland();
    return island;
}
```

<p> &nbsp </p>
 
## How do I get the Island from a specific Location?

You can retrieve an Optional Island from the IridiumSkyblockAPI instance
```java
public Optional<Island> getIsland(Location location) {
    Optional<Island> island = IridiumSkyblockAPI.getInstance().getIslandViaLocation(location);
    return island;
}
```

<p> &nbsp </p>
 
## How do I get the Island from an Island Name?
You can retrieve an Optional Island from the IridiumSkyblockAPI instance
```java
public Optional<Island> getIsland(String name) {
    Optional<Island> island = IridiumSkyblockAPI.getInstance().getIslandByName(name);
    return island;
}
```

<p> &nbsp </p>
 
## How can I see if a Player has permissions to build on an island?

To do this you first need to get the User object from a Player
You can then do this by using the IridiumSkyblockAPI#getIslandPermission function and passing in the correct PermissionType(BLOCK_PLACE)

```java
public boolean canBuild(Island island, Player player) {
    User user = IridiumSkyblockAPI.getInstance().getUser(player);
    boolean isAllowed = IridiumSkyblockAPI.getInstance().getIslandPermission(island, user, PermissionType.BLOCK_PLACE);
    return isAllowed;
}
```

# API (JavaDoc)

<p> &nbsp </p>

## `private IridiumSkyblockAPI(@NotNull IridiumSkyblock iridiumSkyblock)`

Constructor for api initialization.

 * **Parameters:** `iridiumSkyblock` — The instance of the {@link IridiumSkyblock} class

---
 
<p> &nbsp </p>

## `public static @NotNull IridiumSkyblockAPI getInstance()`

Accesses the api instance. Might be null if this method is called when {@link IridiumSkyblock}'s startup method is still being executed.

 * **Returns:** the instance of this api
 * **Since:** 3.0.0

---

<p> &nbsp </p>

## `public void addBankItem(@NotNull BankItem bankItem)`

Adds an Island BankItem.

 * **Parameters:** `bankItem` — The specified Bankitem
 * **Since:** 3.0.0

---
 
<p> &nbsp </p>

## `public void addEnhancement(@NotNull String enhancementName, @NotNull Enhancement<?> enhancement`)

Adds an Island enhancement.

 * **Parameters:**
   * `enhancementName` — The name of the enhancement (used for storage purposes)
   * `enhancement` — the enhancement item
 * **Since:** 4.0.2

---
 
<p> &nbsp </p>

## `public void addPermission(@NotNull Permission permission, @NotNull String key)`

Adds an Island permission.

 * **Parameters:**
   * `permission` — The specified Permission
   * `key` — the unique key associated with this permission
 * **Since:** 3.0.0

---
 
<p> &nbsp </p>

## `public void addCommand(@NotNull Command<Island, User> command)`

Adds an IridiumSkyblock command.

 * **Parameters:** `command` — The command that should be added
 * **Since:** 3.0.0

---
 
<p> &nbsp </p>

## `public @NotNull User getUser(@NotNull OfflinePlayer offlinePlayer)`

Gets a {@link User}'s info. Creates one if they don't exist.

 * **Parameters:** `offlinePlayer` — The player who's data should be fetched
 * **Returns:** the user data
 * **Since:** 3.0.0

---
 
<p> &nbsp </p>

## `public @NotNull Optional<Island> getIslandById(int id)`

Finds an Island by its id.

 * **Parameters:** `id` — The id of the Island
 * **Returns:** Optional with the Island, empty if there is none
 * **Since:** 3.0.0

---
 
<p> &nbsp </p>

## `public @NotNull Optional<Island> getIslandByName(@NotNull String name)`

Finds an Island by its name.

 * **Parameters:** `name` — The name of the Island
 * **Returns:** Optional with the Island, empty if there is none
 * **Since:** 3.0.0
 
---
 
<p> &nbsp </p>

## `public @NotNull Optional<Island> getIslandViaLocation(@NotNull Location location)`

Gets an {@link Island} from a location.

 * **Parameters:** `location` — The location you are looking at
 * **Returns:** Optional of the Island at the location, empty if there is none
 * **Since:** 3.0.0

---
 
<p> &nbsp </p>

## `public @NotNull Optional<Permission> getPermissions(@NotNull String permissionKey)`

Gets a permission object from name.

 * **Parameters:** `permissionKey` — The permission key
 * **Returns:** the permission
 * **Since:** 3.0.0

---
 
<p> &nbsp </p>

## `public @NotNull Optional<Permission> getPermissions(@NotNull PermissionType permissionType)`

Gets a permission object from name.

 * **Parameters:** `permissionType` — The permission key
 * **Returns:** the permission
 * **Since:** 3.0.4

---
 
<p> &nbsp </p>

## `public boolean getIslandPermission(@NotNull Island island, @NotNull User user, @NotNull Permission permission, @NotNull String key)`

Gets whether a permission is allowed or denied.

 * **Parameters:**
   * `island` — The specified Island
   * `user` — The Specified user
   * `permission` — The Specified permission
   * `key` — The permission key
 * **Returns:** true if the permission is allowed
 * **Since:** 3.0.0

---
 
<p> &nbsp </p>

## `public boolean getIslandPermission(@NotNull Island island, @NotNull User user, @NotNull PermissionType permissionType)`

Gets whether a permission is allowed or denied.

 * **Parameters:**
   * `island` — The specified Island
   * `user` — The specified user
   * `permissionType` — The specified permission type
 * **Returns:** true if the permission is allowed
 * **Since:** 3.0.4
 
---
 
<p> &nbsp </p>

## `public @NotNull List<Island> getIslands(@NotNull IslandManager.SortType sortType)`

Gets a list of Islands sorted by SortType.

 * **Parameters:** `sortType` — How we are sorting the Islands
 * **Returns:** sorted list of all Islands
 * **Since:** 3.0.0

---
 
<p> &nbsp </p>

## `public @Nullable World getWorld()`

Returns the overworld.

 * **Returns:** the main Skyblock {@link World}, might be null if some third-party plugin deleted it
 * **Since:** 3.0.0

---
 
<p> &nbsp </p>

## `public @Nullable World getNetherWorld()`

Returns the nether world.

 * **Returns:** the nether Skyblock {@link World}, might be null if some third-party plugin deleted it
 * **Since:** 3.0.0

---
 
<p> &nbsp </p>

## `public @Nullable World getEndWorld()`

Returns the end world.

 * **Returns:** the nether Skyblock {@link World}, might be null if some third-party plugin deleted it
 * **Since:** 3.0.0

---
 
<p> &nbsp </p>

## `public boolean isIslandWorld(@NotNull World world)`

Returns whether the specified world is from IridiumSkyblock.

 * **Parameters:** `world` — The world that should be checked
 * **Returns:** true if it is a world used by IridiumSkyblock
 * **Since:** 3.0.7
 
---
 
<p> &nbsp </p>

## `public boolean isIslandOverWorld(@NotNull World world)`

Returns if this is the overworld of IridiumSkyblock.

 * **Parameters:** `world` — The world that should be checked
 * **Returns:** true if this is the overworld of IridiumSkyblock
 * **Since:** 3.1.3
 
---
 
<p> &nbsp </p>

## `public boolean isIslandNether(@NotNull World world)`

Returns if this is the nether world of IridiumSkyblock.

 * **Parameters:** `world` — The world that should be checked
 * **Returns:** true if this is the nether world of IridiumSkyblock
 * **Since:** 3.1.3

---
 
<p> &nbsp </p>

## `public boolean isIslandEnd(@NotNull World world)`

Returns if this is the end world of IridiumSkyblock.

 * **Parameters:** `world` — The world that should be checked
 * **Returns:** true if this is the end world of IridiumSkyblock
 * **Since:** 3.1.3
 
---
 
<p> &nbsp </p>

## `public boolean canVisitIsland(@NotNull User user, @NotNull Island island)`

Returns whether the specified player can visit the provided Island.

 * **Parameters:**
   * `user` — the user
   * `island` — the Island
 * **Returns:** true if the user can visit the Island
 * **Since:** 3.2.7
  
---

<p> &nbsp </p>

# Island Creation Event

These API calls can be found in ``IslandCreateEvent.java``.

<p> &nbsp </p>

## `@Nullable public String getIslandName()`

The name of the Island.<br> null indicates that the name of the Player is used as the Island name because it hasn't been set.

 * **Returns:** the name of the Island or null

---

<p> &nbsp </p>

## `public void setIslandName(@Nullable String islandName)`

Sets the name of the Island.<br> set it to null to default to the player's name

 * **Parameters:** `islandName` — The name of the island
 
---

<p> &nbsp </p>

## `public void setSchematicConfig(Schematics.@NotNull SchematicConfig schematicConfig)`

Sets the schematic of the new island

 * **Parameters:** `schematicConfig` — The schematic configuration of the island
 
 ---
 
<p> &nbsp </p>

# Island Permission Types
 
-  BLOCK_BREAK
-  BLOCK_PLACE
-  BUCKET
-  CHANGE_PERMISSIONS
-  CLAIM
-  DEMOTE
-  DESCRIPTION
-  DOORS
-  INVITE
-  TRUST
-  KICK
-  KILL_MOBS
-  OPEN_CONTAINERS
-  PROMOTE
-  REDSTONE
-  RENAME
-  SETHOME
-  MANAGE_WARPS
-  SPAWNERS
-  SETTINGS
 
<p> &nbsp </p>

# Island Deletion Event

These API calls can be found in ``IslandDeleteEvent.java``.

<p> &nbsp </p>

