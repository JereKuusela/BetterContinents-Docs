---
layout: default
title: Settings
nav_order: 17
has_children: true
---

# Settings

Settings are separated into two parts:

* **The Config Settings**  
  This contains settings that are not specific to any particularly world.  
  Some are applied always to any active world (debug settings), and some are baked into the world when it is created (the terrain and spawning settings).
* **The World Settings**  
  These are the settings mentioned above, that are 'baked' into the world when it is created. Once baked, they can only be changed using the Console Commands, mentioned below.  
  The World Settings to not usually map directly to the values in the Config Settings, instead they are calculated from them.  
  Example:
  > In the Config Settings the 'Sea Level Adjustment' is specified as a `0` to `1` value, defaulting to `0.5`, whereas the actual value generated in the World Settings is an absolute one from `-0.25` to `+0.25`, which is then multiplied by `200` in the height generation algorithm to give a final value in meters of `-50` m to `+50` m.  
  So `0` Sea Level Adjustment in the Config Settings translates to `-50 m` change in Sea Level in game.  
  You don't need to worry too much about this, just use the Console Commands below for tweaking these values, and you can immediately see what it looks like in game.  

## BepInEx Configuration Manager

Config Settings can be accessed via the in game BepInEx Configuration Manager (see the [Setup Guide](../setup-guide.html) for installation instructions).  
It is opened by pressing F1, after which you can see sections for each BepInEx mod you have installed. Just click the sections to expand them, then change the settings.  
> Note: There is no "save" or "apply" button, the settings are saved automatically.

## BepInEx Config File

You can also access the Config Settings in the config file itself. This is in the `BepInEx\config` directory in your Valheim installation directory. After running the game once with Better Continents installed the config file will be generated.

## Console Commands

When you are loaded into a world that was created with Better Continents enabled, you can use an extensive set of console commands to modify the World Settings.  
Open the Console with F1 (this mod enables it always), and then enter `bc` to get help on the basic commands. See the specific settings in this documentation (they are organised by group) for examples and documentation for each command.
