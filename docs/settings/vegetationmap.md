---
layout: default
title: Vegetation map
nav_order: 8
---

## Vegetation map

The vegetation map allows you to control where vegetation (trees, bushes, rocks, and other objects) appears in the world. You can enable or disable vegetation for different areas using specific colors.

## Vegetation map File

{: .d-inline-block }
Setting
{: .label .label-green }

Path to a vegetation map file to use.

### Requirements

See [Image Requirements](../faq.html#what-are-the-image-requirements-for-map-files) for the size and format requirements.  
24 bit RGB PNG of medium resolution would be a sensible format for a vegetation map.

### Configuration

Vegetation maps work together with a text file (`vegetationmap.txt`) that defines what each color means.

**Color behavior:**

* **Black color** (`#000000`) is hardcoded to be no change - uses default vegetation behavior
* **White color** (`#FFFFFF`) is hardcoded to disable all vegetation in that area
* **Other colors** can be configured in `vegetationmap.txt` to specify which vegetation should appear

### Vegetation Map Text File

The `vegetationmap.txt` file defines what happens for each color in your vegetation map. Each line follows this format:

```yaml
RRGGBB: object1, object2, -object3, all, none
```

**Special keywords:**

* `all` - enables all vegetation
* `none` - disables all vegetation  
* `-ObjectName` - disables a specific vegetation object (note the minus sign)

**Rules:**

* Enabling vegetation sets the biome requirement to any biome, affecting the whole 64m x 64m zone
* Disabling vegetation uses a more precise "clear area" system
* Commands are processed in order, so you can combine `all` with specific disables

### Examples

```yaml
# Red color enables only Beech trees and Rocks
FF0000: none, Beech1, Rock4_forest

# Blue color disables all vegetation but enables Pine trees
0000FF: none, FirTree

# Green color enables all vegetation but disables rocks
00FF00: all, -Rock1_forest, -Rock2_forest, -Rock3_forest, -Rock4_forest

# Yellow color creates sparse forest (only some trees)
FFFF00: none, Beech, FirTree, Pine_tree

# Purple color removes all trees but keeps bushes and rocks
800080: all, -Beech, -FirTree, -Pine_tree, -Birch
```

### Common Vegetation Objects

Some common vegetation object names you can use:

* **Trees:** `Beech`, `FirTree`, `Pine_tree`, `Birch`
* **Rocks:** `Rock1_forest`, `Rock2_forest`, `Rock3_forest`, `Rock4_forest`
* **Bushes:** `BlueberryBush`, `Raspberry`
* **Other:** `Mushroom`, `Thistle`, `Dandelion`

### Creation Tips

* Use high contrast colors that are easy to distinguish
* Test your vegetation map in-game to see the results
* Remember that vegetation changes affect 64m x 64m zones, not individual pixels
* Use the minus prefix (`-`) to disable specific objects when using `all`
* Consider performance - dense vegetation can impact framerate

<details class="console" markdown="block">
<summary>
Console
</summary>
Command: `bc param vm fn`
<img src="../images/console/bc-param-v-fn.gif" />
</details>
