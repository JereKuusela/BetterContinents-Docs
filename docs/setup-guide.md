---
layout: default
title: Setup Guide
nav_order: 3
---

# Setup Guide

## Client
Ideally use [Vortex](https://www.nexusmods.com/about/vortex/) to install, as it includes all the dependencies you need for this mod already.

Otherwise do this:
1. **Backup your world saves**. Do it. Do it now! Backup your characters aswell while you are at it.
1. **Install [BepInEx Valheim](https://valheim.thunderstore.io/package/denikson/BepInExPack_Valheim/)**.
1. **Install [Better Continents](https://www.nexusmods.com/valheim/mods/446?tab=files)** itself: place the `BetterContinents.dll` in the `BepInEx\plugins` directory.

Optional but recommended if you want to make new worlds yourself:
1. **Install the [BepInEx Configuration Manager](https://github.com/BepInEx/BepInEx.ConfigurationManager/releases)**. This gives you UI in game for changing configuration, otherwise you will need to edit text files to change settings.
1. **Install the [SkToolbox](https://www.nexusmods.com/valheim/mods/8)**. This gives improved console behaviour that makes iterating on a new world a nicer experience.

## Dedicated Server
1. **Stop your server.**
1. **Backup your world saves** on from server. Do it. Do it now!<br>How you access them depends on your provider, probably ftp. Download them locally and put them somewhere safe.<br>Each world should have a `.fwl` and `.db` file, and the default world is called `Dedicated`.<br>On Linux servers the world files should be found at `.config/unity3d/IronGate/Valheim/worlds`, on Windows servers at `%AppData%\..\LocalLow\IronGate\Valheim\worlds` (same as for Windows clients).
1. **Enable mods on your server** if they are not enabled already.<br>How to do this is highly dependent on your server provider: for instance some have a toggle on the server management page to "enable mods", which results in BepInEx (or a mod that comes with BepInEx, e.g. Valheim+) being installed and enabled for you. Alternatively you might need to set this up yourself, in which case you should follow [BepInEx server installation guide](https://valheim.thunderstore.io/package/denikson/BepInExPack_Valheim/).
1. **Upload this mod** to the `BepInEx\plugins` directory on your server. Again this depends on your server provider, but probably you will do it by FTP. The `BetterContinents.dll` file should now reside in the `BepInEx\plugins` directory.
1. **Upload the world** you want to use that was created with Better Continents, perhaps one from [here](https://www.nexusmods.com/valheim/mods/categories/13/), or one you created your self. Its possible to create a new world ON the server, but it is easier to do it locally as you can modify the configuration in game and test it first.
    > NOTE: Some providers don't allow any files other than `.fwl` and `.db` to be uploaded. This will not work, you must also upload the `.BetterContinents` file. Complain to your server provider, or switch to another one!
1. **Point your server at the world** you uploaded. How to do it depends on your server provider, there should be some mechanism to specify the World Name, or modify the command line of the server.
1. **Start your server again** and join it.

### **IMPORTANT**: You need to follow the [Client setup guide](setup.html) as well!
Both client **and** server need the same version of Better Continents installed when running a Better Continents world.  
However: you can join servers that don't have Better Continents installed without it interfering (it will just be disabled).  
You can also join servers that have Better Continents installed, without having it installed yourself, *as long as the server runs a world that doesn't require it* (i.e. one created without it).
