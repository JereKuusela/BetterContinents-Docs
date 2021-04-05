---
layout: default
title: Introduction
nav_order: 1
---

# Introduction

This mod provides the tools to both improve the standard heightmap generation of the game, and override aspects of it with hand crafted height and biome maps taken from images.  
These generated worlds can be shared with others by simply copying the usual world files, along with the extra `.BetterContinents` file this mod stores its own settings in.  
This mod must be installed anywhere the world is to be used, it won't work correctly without it.

# Features
* Use image files as [base heightmap](settings/heightmap.html#heightmap-file) layer, [detail heightmap](settings/flatmap.html#flatmap-file) layer, and [biome specific heightmap](settings/roughmap.html#roughmap-file) layer, with blending options for each
* Use an [image file to specify biomes](settings/biomemap.html#biomemap-file)
* Use an [image file to specify spawning positions](settings/spawnmap.html#spawnmap-file) for locations, including player start, bosses, and trader
* Use an [image file to specify forest coverage](settings/forest.html#forestmap-file), including in [biomes that normally are totally forested](settings/forest.html#forest-factor-overrides-all-trees) (Swamp, Mistlands, Dark Forest, Mountains)
* Change [global scale](settings/global.html#continent-size) -- changes continent sizes
* Adjust [mountains amount](settings/global.html#mountains-amount)
* Adjust [sea level](settings/global.html#sea-level-adjustment)
* Adjust [forest scaling](settings/forest.html#forest-scale) (how big the contiguous areas of forest/clearings are), and amount
* Specify [starting position](settings/start-position.html) explicitly
* Additional customizable [ridged heightmap layer](settings/ridges.html) gives more varied geography
* Still allows loading vanilla maps, without needing to adjust any settings or disable the mod
* Backwards compatible (since version 0.2) -- worlds created with older versions will still look the same when loaded with newer ones
* Includes a debug mode to automatically enable cheats, reveal the full map, toggle on vanilla debugmode, and various other things, for quicker testing
* Allows skipping of default location placement for quick world generation
* Has extensive console command list for adjusting all settings, and regenerating locations
* Custom map update when using console commands allows changes to be seen in full in a matter of seconds
* Export full map to png at any resolution

# Useful Links
[Better Continents](https://www.nexusmods.com/valheim/mods/446) on Nexusmods

Join the [Valheim Worlds discord](https://discord.gg/3XW8ZntYzN) to get help, share progress or tips and tricks.

See maps people have shared on [Nexusmods.com here](https://www.nexusmods.com/valheim/mods/categories/13/).

