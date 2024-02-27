---
title: Member Permissions
description: An explanation on Island Member permissions and how they work.
published: true
date: 2023-10-12T17:14:11.636Z
tags: 
editor: undefined
dateCreated: 2023-08-09T13:21:43.200Z
---

# Permission Configuration

> Note: This page is for information regarding Island Member ranks, which are different than the permissions you give to players or ranks via a permissions plugin. Please see our [Commands & Permissions](https://docs.iridiumdevelopment.net/en/Commands-&-Permissions) page for more details.
{.is-warning}

<p> &nbsp </p>

## Creating Island Ranks

The Island Member rank system works by defining ranks to go in between the `Visitor` rank and the `Owner` rank. These ranks will be ordered numerically as defined in `configuration.yml`, with the lower value typically being representative of a lower rank.

<details>
  <summary> Visitor & Owner Rank configuration </summary>

While the `Visitor` rank has no permissions by default, these can be changed by anyone who has the `changePermissions` permission. In contrast, the `Owner` rank has all permissions by default, and this cannot be changed.

```yaml
visitor:
  name: "Visitor"
  item:
    material: "WOODEN_AXE"
    amount: 1
    displayName: "&7&lVisitor"
    headData: null
    headOwner: null
    headOwnerUUID: null
    model: null
    lore: []
    slot: 11
owner:
  name: "Owner"
  item:
    material: "DIAMOND_AXE"
    amount: 1
    displayName: "&c&lOwner"
    headData: null
    headOwner: null
    headOwnerUUID: null
    model: null
    lore: []
    slot: 15
```

> *The default configuration for the `Vistor` and `Owner` ranks in `configuration.yml`.*
---

- **rank**: The rank category for configuration.
  - *name*: ^[String]^ The name of the rank.
    - *item*: ^[Object]^ The item category that determines how the rank shows up in `/is permissions`. For more information, please see our [Inventory & Menus](https://docs.iridiumdevelopment.net/en/Inventory) page.
  
</details>

<details>
  <summary> Member Ranks </summary>

  The main difference between Island Member ranks and the Visitor/Owner ranks is that these ranks have numerical IDs attached to them. They are slotted in between Visitor and Owner, and you can configure as many or as few as you'd like for your players to assign. The numerical IDs assigned to ranks in this section is used in `permissions.yml` to set default permissions for each rank, and a higher value rank will inherit permissions from a lower value rank. 
  
  In this example, the `Member` rank is configured and assigned the numerical ID of `1`, so any permission with `defaultRank` set to `1` will be assigned to the `Member` rank by default.
  
```yaml
userRanks:
  1:
    name: "Member"
    item:
      material: "STONE_AXE"
      amount: 1
      displayName: "&9&lMember"
      headData: null
      headOwner: null
      headOwnerUUID: null
      model: null
      lore: []
      slot: 12
```
> *The default configuration for the "Member" rank in `configuration.yml`.*
---

- **userRanks**: The player ranks category for configuration.
  - *rank*: ^[int]^ The numerical ID number for the rank.
  - *name*: ^[String]^ The name of the rank.
    - *item*: ^[Object]^ The item category that determines how the rank shows up in `/is permissions`. For more information, please see our [Inventory & Menus](https://docs.iridiumdevelopment.net/en/Inventory) page.

</details>


<p> &nbsp </p>

## Assigning Permissions

```yaml
blockBreak:
  item:
    material: "DIAMOND_PICKAXE"
    amount: 1
    displayName: "&9Break Blocks"
    headData: null
    headOwner: null
    headOwnerUUID: null
    model: null
    lore:
    - "&7Grant the ability to break any blocks in your Island."
    - ""
    - "&9&lPermission"
    - "%permission%"
    slot: 10
  page: 1
  defaultRank: 1
```
> *The default configuration for the blockBreak permission in `permissions.yml`.*

---

- **Permission**: The permission category for its configuration.
  - *item*: ^[Object]^ The item category that determines how the permission shows up in `/is permissions`. For more information, please see our [Inventory & Menus](https://docs.iridiumdevelopment.net/en/Inventory) page.
  - *page*: ^[int]^ The page that the permission should be displayed on in the menu.
  - *defaultRank*: ^[int]^ The numerical ID for the rank that this permission comes with.