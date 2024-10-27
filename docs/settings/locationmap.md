---
layout: default
title: Location map
parent: Color maps
nav_order: 3
---

# Location map

The spawnmap allows you to control where locations are placed when the world is created. The Spawn color chart below shows the various types of location that are supported, including all the start location, bosses, trader, and dungeons.

## Location

{: .d-inline-block }
Setting
{: .label .label-green }

Path to the locationmap.png file (32 bit RGBA. medium resolution) and the locationmap.txt file.

Notes:

* The image background should be black.
* The location map colors must match *exactly* with the one specified in the locationmap.txt file. Usually this shouldn't be a problem if you use high quality png.
* The actual location position is chosen from all adjacent pixels in the spawnmap that have the same color. i.e. Every contiguous (not including diagonal) area of the same color is a single location, the final position of which is a randomly chosen pixel from with the area. So you need to separate spawn areas by at least one pixel of black to stop them registering as the same area.


### Location map Behaviour

* All location positions specified in your location map will be filled, even if they exceed the max number expected by the game, so you can always be sure that all your locations will be filled.
* The game will try and place all locations, prefering using the location map first, then using its own placement system. The only way to have ONLY location map positions filled is to place the same amount or more than the game wants to place. If you don't want that many on the map, then place them in the corners of the map where players cannot see or reach.

### Location map Creation Hints

* Bring the spawn color table into your paint tool as a separate layer, or tabbed image, for easy access. Use the eye dropper on it to quickly select a spawn color.
* Draw spawn areas using a pencil tool NOT brush, as you want a hard edge and no color variation. Use a size that can be seen easily without having to zoom in. Slight randomization of the spawn location won't matter (see the example images).
* Place your heightmap/biomemap background layers so you can easily see where you are placing spawns.
* Use a separate layer for each spawn type (bosses, markers, buildings etc.), then you can easily change the type of all of them in one go.

<details class="console" markdown="block">
<summary>
Console
</summary>
Command: `bc param s fn`
<img src="../images/console/bc-param-s-fn.gif" />
</details>
