---
layout: default
title: Spawn map
nav_order: 7
---

## Spawn map

The spawn map allows you to control where creatures spawn in the world. You can enable or disable spawns for different areas using specific colors.

## Spawn map File

{: .d-inline-block }
Setting
{: .label .label-green }

Path to a spawn map file to use.

### Requirements

See [Image Requirements](../faq.html#what-are-the-image-requirements-for-map-files) for the size and format requirements.  
24 bit RGB PNG of medium resolution would be a sensible format for a spawn map.

### Configuration

Spawn maps work together with a text file (`spawnmap.txt`) that defines what each color means.

**Color behavior:**

* **Black color** (`#000000`) is hardcoded to be no change - uses default spawn behavior
* **White color** (`#FFFFFF`) is hardcoded to disable all spawns in that area
* **Other colors** can be configured in `spawnmap.txt` to specify which creatures should spawn

### Spawn Map Text File

The `spawnmap.txt` file defines what happens for each color in your spawn map. Each line follows this format:

```
RRGGBB: creature1, creature2, -creature3, all, none
```

**Special keywords:**

* `all` - enables all spawns
* `none` - disables all spawns  
* `-CreatureName` - disables a specific creature (note the minus sign)

**Rules:**

* Enabling spawns sets the biome requirement to any biome, affecting the whole 64m x 64m zone
* Disabling spawns uses a more precise "clear area" system
* Commands are processed in order, so you can combine `all` with specific disables

### Examples

```yaml
# Red color enables Wolves and Skeletons to spawn in that area
FF0000: Wolf, Skeleton

# Blue color disables all spawns but enables Wolves and Skeletons
0000FF: none, Wolf, Skeleton

# Green color enables all spawns but disables Wolves and Skeletons
00FF00: all, -Wolf, -Skeleton

# Yellow color enables all creatures except Trolls
FFFF00: all, -Troll

# Purple color only allows Greydwarfs
800080: none, Greydwarf
```

### Creation Tips

* Use high contrast colors that are easy to distinguish
* Test your spawn map in-game to ensure creatures spawn as expected
* Remember that spawn changes affect 64m x 64m zones, not individual pixels
* Use the minus prefix (`-`) to disable specific creatures when using `all`

<details class="console" markdown="block">
<summary>
Console
</summary>
Command: `bc param sm fn`
<img src="../images/console/bc-param-s-fn.gif" />
</details>
