---
layout: default
title: Heightmap
parent: Settings
nav_order: 3
---

# Heightmap
{: .no_toc }

<details open markdown="block">
  <summary>
  Contents
  </summary>
  {: .text-delta }
1. TOC
{:toc}
</details>

---

## Heightmap File
Path to a heightmap file to use.

### Requirements
* The height map image must be square, and one of these sizes: 32. 64, 128, 256, 512, 1024, 2048, 4096.
* Most formats are supported, including HDR ones (anything Unity Texture Import supports). 

### Where to get Heightmaps
* Craft them from scratch in some package. People have used Photoshop, Krita, GIMP, Blender to good affect. 
* [Google](https://www.google.com/search?q=heightmap%20images&tbm=isch&tbs=rimg%3ACUrn-Sh_19QfyYckcSKAP9V2W&biw=1838&bih=1019)
* This very nice [Google Maps style page](https://tangrams.github.io/heightmapper) that will export heightmaps directly for any area on Earth.
* [World Machine](https://www.world-machine.com/): This is highly advanced heightmap generating software that can do things like physical modelling of erosion. It can also generate assist in generating biome maps automatically as well.
* [Gaea](https://quadspinner.com/): Similar to World Machine, might be quicker to get started with. 

### Creation Hints
* Ensure the ocean areas of the heightmap are pure black, not grey
* Apply automatic contrast/levels to ensure the values are using the full range available
* I recommend smoothing (blurring) the image to avoid any sharp changes in altitude
* Getting sealevel looking correct might take some tweaking, of either the image itself or the sealevel setting
* To determine sealevel with your current config settings you can create a smooth gradient on the heightmap (gradient paint bucket tool in Photoshop), apply a flatish biome to it (e.g. plains), and then view it in game to determine what gray value corresponds to sealevel. In my testing with sealevel set to 25% the corresponding gray value is about #0d0d0d.
* When trying to test your map in game start with all default, then set these settings:
  * [Heightmap File](heightmap.html#heightmap-file) - paste your file name in here, or use the [Project Directory](project.html#directory) with an appropriate heightmap file in it.
  * [Ocean Channels](global.html#ocean-channels) un-ticked
  * [Rivers](global.html#rivers) un-ticked
  * [Ridges Amount](ridges.html#ridges-amount) 0%

## Heightmap Amount
Multiplier of the height value from the heightmap file (more than 1 leads to higher max height than vanilla, good results are not guaranteed).  

> Default `1`  
> Range `0` to `5`

## Heightmap Blend
How strongly to blend the heightmap file into the final result.  

> Default `1`  
> Range `0` to `1`

## Heightmap Add
How strongly to add the heightmap file to the final result (usually you want to blend it instead).  

> Default `0`  
> Range `-1` to `1`
