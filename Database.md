---
title: Database
description: This page details how to setup SQL with IridiumSkyblock, and how its stores data.
published: true
date: 2024-02-18T15:07:06.926Z
tags: 
editor: markdown
dateCreated: 2023-09-24T19:40:04.043Z
---

# Database

IridiumSkyblock uses SQL to store its player data in the ``IridiumSkyblock.db`` file. This means that this file contains tables with data on players and their islands.

In order to reset player data for IridiumSkyblock, you just need to delete this file, as IridiumSkyblock will regenerate it on launch.

In order to use your own SQL server with IridiumSkyblock, you need to provide the plugin with the details of the server, which can be done in ``sql.yml``. By default, this file will create a local instance of the database file in ``plugins/IridiumSkyblock``.

```yaml
---
driver: "SQLITE"
host: "localhost"
database: "IridiumSkyblock"
username: ""
password: ""
port: 3306
useSSL: false
````
> *The default configuration for ``sql.yml``.*


- *driver*: ^[enum]^ The type of SQL used to store data. Currently only supports SQLite.
- *host*: ^[String]^ The IP of the server housing the SQL data.
- *database*: ^[String]^ The name of the database file.
- *username*: ^[String]^ The username needed to access the database server.
- *password*: ^[String]^ The password needed to access the database server.
- *port*: ^[int]^ The port that the server is being hosted on.
- *useSSL*: ^[boolean]^ Whether the server uses SSL.