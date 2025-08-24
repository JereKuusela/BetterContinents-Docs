---
layout: default
title: Paint map
nav_order: 9
---

## Paint map

The paint color is applied on top of the ground texture. This is used for player placed modifications like paving and cultivation.

However Mistlands and Ashlands also use this system for the alternative moss ground and lava.

To make editing easier, the default moss and lava generation is used when the color is fully opaque.

Different paints can be mixed but the ratios are not intuitive.

| Paint         | Color       |
|:-------------:|:-----------:|
| Grass         | `#000000FF` |
| Dirt          | `#FF0000FF` |
| Cultivated    | `#00FF00FF` |
| Paved         | `#0000FFFF` |
| Moss          | Depends on the alpha value |
| Lava          | When alpha > 99 |
| Patches       | `#00BF00FF` |
| Grass Dark    | `#996600FF` |
| Paved Moss    | `#000080FF` |
| Paved Dirt    | `#FF0080FF` |
| Paved Dark    | `#00FF80FF` |
| ...    | Experiment |

Note: Players can't modify the alpha channel, so using it on other biomes affects their terrain editing.

## Moss and lava

Alpha channel can be difficult to use with some image editors. There are two ways around this:

- Use the mossmap.png and lavamap.png files for these features.
  - This is recommended if you don't have use for other paints.
- Use the paintmap.txt file to map opaque colors to the alpha channel.

Following rules apply:

1. If the moss map exists and the biome is Mistlands, alpha value comes from the moss map.
2. If the lava map exists and the biome is Ashlands, alpha value comes from the lava map.
3. If the paint color is fully opaque, alpha value comes from the default generation.
4. Otherwise alpha value comes from the paint color.

## Paint file

{: .d-inline-block }
Setting
{: .label .label-green }

Path to the paintmap.png file (32 bit RGBA) and the paintmap.txt file.
