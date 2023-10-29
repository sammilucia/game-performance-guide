# General Game Performance (Optimisation) Guide (GGPOG)

I previously published this with some mods, but it applys to most games, so I'm moving it here as a general resource.

## Contributing

Do it.

## General Game Performance Optimisation

### 1. Install games on an SSD wherever possible

Generally, new games use some form of resource streaming (whether they're aware of it or not). Most new games will attempt to load game assets as you move through the game. For this reason, not using an SSD will cause performance problems.

### 2. Disable VSync in-game (new games)

This will vary from game to game, but more and more new games will use (DXGI flip presentation)[https://devblogs.microsoft.com/directx/dxgi-flip-model/]

### 3. Make sure not too much is running in the background in Windows (or Linux, etc.)

(Required) On the first graphics settings page about 2/3 down, click Image Calibration and follow the instructions. This sets your black point. If the game is too dark for you, come back to this page and nudge it around
(Recommended) in Windows -> Display Settings -> Graphics Settings (at the bottom) -> Enable Hardware-accelerated GPU scheduling. Also enable Variable refresh rate if you have it
(Strongly recommended) Disable Control Flow Guard in Windows. Click Start > type Exploit Protection > Click Program Settings > Click Add program to customize > click Add by program name > type HogwartsLegacy.exe > Scroll down to Control flow guard (CFG) > Click Override > Switch it to Off. Done! You should get even fewer hitches. If the game was running you need to restart it
(Optional) Update the DLSS DLL (version 3.1.13 is included with the mod). You really won't notice much difference though
(Required) Raytraced reflections require DLSS or DLAA, or FSR in this game
(Required) If you're using any raytracing in-game, set the RT quality to Ultra. I've clamped performance optimisations for RT in the mod. Changing RT from Ultra won't give you any more performance, but it will probably break things.
(Recommended) Ultra+ now completely disables the the Ryzen Chroma DLL plugin — you no longer need Stuttering and Low Performance Fix﻿ (SLPF)
(Optional) enable resizable bar if you can. This game copies a LOT from CPU to GPU. It's not necessarily about CPU cores but it's definitely about CPU to GPU bamdwidth. Even a reBar of 1 or 2GB can helps
(Recommended) disable PCI Express Link State Power Management in Windows Power Plans (here's how﻿). No this isn't the root cause problem, but enabling as much CPU > GPU bandwidth as possible helps this and other games
(Recommended) if you're due to update your video drivers, use Display Driver Uninstaller﻿ (DDU) in Safe Mode to completely remove the old drivers and reinstall from scratch. It shouldn't... but I still hear of games being fixed by this. I recommend the NVidia Studio Drivers, or AMD Recommended drivers, because they're fully tested 
