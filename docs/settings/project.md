---
layout: default
title: Project
parent: Settings
nav_order: 2
---

# Project
The project setting allows the use of standardized names for the image maps to enable automatically using them from a specified directory.

---
## Directory
This directory will load automatically any existing map files matching the correct names, overriding specific files specified below.  

Only png is supported using this method, however png is the recommended format in general as it supports both 16 bit grayscale, and 8 bit RGB, and these cover the requirements of all the image types.  

If you specify a directory, the specific file path settings are all ignored, even if the project directory doesn't contain a file that would override them. i.e. You can *either* specifiy a Project Directory and follow these naming conventions, OR you must specify each file path separately using its associated setting (in the table below). You can't mix these methods.

### Filenames 
| File Name | Target Setting |
|:---|:---|
| `heightmap.png` | [Heightmap File](settings/heightmap.html#heightmap-file) |
| `roughmap.png` | [Roughmap File](settings/roughmap.html#roughmap-file) |
| `flatmap.png` | [Flatmap File](settings/flatmap.html#flatmap-file) |
| `biomemap.png` | [Biomemap File](settings/biomemap.html#biomemap-file) |
| `forestmap.png` | [Forestmap File](settings/forest.html#forestmap-file) |
| `spawnmap.png` | [Spawnmap File](settings/spawnmap.html#spawnmap-file) |
