---
layout: default
title: Quick Start
nav_order: 2
---

# Quick Start

## For Players
Just follow the setup guide, it also explains how to upload worlds to your server.  

That should be it.  

## For Authors
1. Follow the setup guide
2. For a working example examine [my example map](https://www.nexusmods.com/valheim/mods/616) which includes the source Photoshop file as a separate download.
3. To see an example of authoring a new map from scratch see [this video](https://www.youtube.com/watch?v=SuDieAlR6Kg) in which I use my [template file](https://www.nexusmods.com/valheim/mods/446?tab=files). Use the chapters to see different parts of the process I am using.
4. To see how to take the exported image files from the previous step into the game, and create and verify the world see [this other video](https://www.youtube.com/watch?v=MzO_cl_mTLA).
5. Check out the [settings](./settings/settings.html) so find out what the different config parameters do, and how to apply them using the console to a world, while in game.

### Tools
I would recommend using Photoshop or [Krita](https://krita.org/en/download/krita-desktop/) for authoring, NOT GIMP, as GIMP does not support [non-destructive editing](https://helpx.adobe.com/uk/photoshop/using/nondestructive-editing.html) via layer effects.
Krita is open source, and has a mostly identical layer effects system to Photoshop.
If you have a tablet then it can help a lot in painting smoothly and organically.
You could use [World Machine](https://www.world-machine.com/) or [Gaea](https://quadspinner.com/) to either generate a new heightmap, or modify an existing one. The erosion effects alone can help you make the terrain a lot more realistic, and be a guide on river placement. You could also generate biomemaps using it, but I won't be going into that here (it is a complex subject and I have not investigated it in any depth).

### Template
I recommend you use my [template file](https://www.nexusmods.com/valheim/mods/446?tab=files) as a starting point.
It contains premade groups, with height, water, and biome layers already setup.
The intended usage of the groups\layers is like so:

* Heightmap\Heightmap: this is your base heightmap, paint it, paste something in, however you want to create it. The mask should be white for land and black for water (we can call this a "land mask"). You can generate the inital land mask using Threshold on the heightmap.
* Heightmap\Water edge mask: this is intended for creating smooth transitions between water and land, i.e. avoiding cliffs. The mask should be white for water, black for land (we can call this the "water mask"). i.e. This mask is the inverse of the land mask, and you can create it just by coping the land mask, then applying color invert.
* Biomes: the rest of the layers are the biomes themselves. Just paint white into the mask to apply that biome. You can use soft brush/smudge etc and then apply threshold to the mask directly to get crisp edges back again (which is required for it to load correctly).
* Reference: this contains reference images. Its often useful to drop in the source map you are trying to recreate, then set it as semi-transparent so you can paint over/under it. For my Middle Earth map I also dropped in a reference image that showed the route followed by Frodo/Bilbo so I could mark it with waymarkers in the spawnmap.
* Reference\Biome Key: this is just a reference for the biome colors, you don't need it really as the layers are already set up.
* Reference\Spawn Table: this is the key for how colors map to what is spawned. Where the same color maps to multiple things which one is 
used will be randomly selected on world creation. I did this to simplify the spawnmap creation process, and make it easier to read visually. If there are some in there that should not be grouped then please raise in the comments.[*]Spawn: this is your primary spawnmap layer. I suggest you put the main spawns in here (starting point, bosses, trader), and then add extra layers for things of which there are many. e.g. a layer for buildings, one for waymarkers, etc. I suggest you paint them in using 3 radius pencil (or bigger if you want more randomness). Ensure the spawn areas don't touch each other.
* Source: this is a place for your source images. You should put them in here to start with, and never modify them, rather copy them when you need to. Its always useful to be able to reference the unmodified source directly.
