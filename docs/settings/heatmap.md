---
layout: default
title: Heatmap
nav_order: 13
---

## Heat map

The Ashlands biome uses heat feature to make the water deal damage to ships and players.

By default, the boiling area matches the default generation of Ashlands biome. If you want to have boiling water somewhere else then you need to use the heat map.

Heat has intensity that affects how much damage is dealt to ships and how fast the player starts burning.

By default, the intensity increases when moving deeper into the Ashlands. Most effects cap after 300 meters when the intensity reaches 1. When partially standing on water, the effect caps after 3000 meters when the intensity reaches 10.

The heat map uses 10x scaling, so the max value of white color means 10 intensity.

## Heat file

{: .d-inline-block }
Setting
{: .label .label-green }

Path to the heatmap.png file (16 bit greyscale).

## Heat scale

{: .d-inline-block }
Setting
{: .label .label-green }

Heat map scaling. Default is 10.
