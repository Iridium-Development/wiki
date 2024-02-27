---
title: Translation
description: A guide on how to translate the plugin.
published: true
date: 2023-09-29T13:32:42.798Z
tags: 
editor: undefined
dateCreated: 2023-08-09T16:47:33.837Z
---

> Note: Always make a backup of your configuration files before reloading the plugin to use them.
{.is-warning}


# Required Reading

Translating IridiumSkyblock takes time and a lot of patience, unfortunately, but it is entirely possible.

Messages for the plugin are stored in `messages.yml`, and the GUI text can be found in `inventories.yml`. If you need to translate other parts of the plugin, check what section you're working on for its tooltip message (lore).

All Translations must follow these rules:

1. All files MUST be in `UTF-8` encoding for the plugin to recognize it.
2. All files accept `unicode` characters.
3. All files MUST be valid `yaml` files.

![translation-example-utf-8.png](/translation-example-utf-8.png)

> *A screenshot of the footer in VS Code, identifying the current file as a UTF-8 YAML file.*

> Note: Do not translate placeholders. They will not show the information you need if you do.
> Placeholders look like this: `%placeholder%`.
{.is-info}

> Note: In order to download and use default configurations that are listed on this page, you will need [7zip](https://www.7-zip.org/) or an equivalent archival program capable of opening `.7z` files.
{.is-info}


# Example:

<p> &nbsp </p>

## Default (English)

```yaml
helpCommandFooter: " &7Page %page% of %max_page% "
```

![translation-example-english.png](/translation-example-english.png)

> *A screenshot of the page indicator from `/is help`, English translation.*
> *You can download the default configuration [here](/default-config-english-iridiumskyblock.7z).*

---

<p> &nbsp </p>

## Español (España)

```yaml
helpCommandFooter: " &7Página %page% de %max_page% "
```

![translation-example-spanish.png](/translation-example-spanish.png)

> *Una captura de pantalla de la indicador página de `/is help`, traducción Español (España).*

---

<p> &nbsp </p>

## Deutsche

```yaml
helpCommandFooter: " &7Seite %page% von %max_page% "
```

![translation-example-german.png](/translation-example-german.png)

> *Ein Screenshot der Seitenanzeige von `/is help`, deutsche Übersetzung.*
> *Du kannst die Standard-Konfiguration in deutsch [hier](/default-config-german-iridiumskyblock.7z)  herunterladen. (provided by @dedpohl, thank you!).*

---