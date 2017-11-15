# Minecraft (Craft)

## Background

A simple Minecraft clone written in C using modern OpenGL (shaders).

### Features

* Simple but nice looking terrain generation using simplex noise.
* Biomes
* Water
* More than 20 types of blocks and more can be added easily.
* Supports plants (grass, flowers, trees, etc.) and transparency (glass).
* Simple clouds in the sky (they don't move).
* Day / night cycles and a textured sky dome.
* More sophisticated sunrise/sunset color blending
* Ambient occlusion for basic shading of blocks.
* World changes persisted in a sqlite3 database.
* Configurable draw distance. The draw distance has a big effect on the framerate, a draw distance of 1 or 2 can make this core playable even on very lightweight computers.
* Configurable field of view.
* Gamepad support (including analog stick support) configurable analog sensitivity and deadzones, preliminary mouse and keyboard support.
* Configurable resolutions, up to 4K.
* A ‘Jumping Flash’ mode that allows you to jump infinitely into the air all while the camera faces downwards.

### Author(s):

Snes9x Team|dking|BassAceGold|ShadauxCat|Nebuleon

## Contribute to this documentation

In order to propose improvements to this document, [visit it's corresponding source page on github](https://github.com/libretro/docs/tree/master/docs/library/craft.md). Changes are proposed using "Pull Requests."

## License

MIT

## Extensions

The Craft core does not feature extension use. Just load and start the core.

## Features

| Feature           | Supported |
|-------------------|:---------:|
| Saves             | ✔         |
| States            | ✕         |
| Rewind            | ✕         |
| Netplay           | ✕         |
| RetroAchievements | ✕         |
| RetroArch Cheats  | ✕         |
| Native Cheats     | ✕         |
| Controllers       | ✔         |
| Remapping         | ✕         |
| Multi-Mouse       | ✕         |
| Rumble            | ✕         |
| Sensors           | ✕         |
| Camera            | ✕         |
| Location          | ✕         |
| Subsystem         | ✕         |

The Craft core's directory name is 'Craft'

World data is saved/loaded to and from 'craft.db' in RetroArch's system directory.

## Core options

*The Craft core has the following option(s) that can be tweaked from the core options menu. The default setting is bolded.*

- **Resolution (restart)** (**640x480**/320x200/640x400/960x600/1280x800/1600x1000/1920x1200/2240x1400/2560x1600/2880x1800/3200x2000/3520x2200/3840x2400/7680x4320/15360x8640/16000x9000/320x240/320x480/360x200/360x240/360x400/360x480/400x224/480x272/512x224/512x240/512x384/512x512/640x224/640x240/640x448/720x576/800x480/800x600/960x720/1024x768/1280x720/1366x768/1600x900/1920x1080/2048x2048/4096x4096): Configure the resolution.

??? note "Resolution - 320x240"
	![320x240](images\Cores\craft\320x240.png)
	
??? note "Resolution - 1920x1080"
	![1920x1080](images\Cores\craft\1920x1080.png)	

- **Show info text** (**Off**/On): Show game information in the upper left corner of Craft.

??? note "Show info text - Off"
	![show_info_text_off](images\Cores\craft\show_info_text_off.png)
	
??? note "Show info text - On"
	![show_info_text_off](images\Cores\craft\show_info_text_on.png)	

- **Jumping Flash mode** (**Off**/On):  Enabling this allows you to jump infinitely into the air all while the camera faces downwards.

- **Field of view** (**65**/70/75/80/85/90/95/100/105/110/115/120/125/130/135/140/145/150): Configure the field of view.

??? note "Field of view - 65"
	![fov_65](images\Cores\craft\fov_65.png)
	
??? note "Field of view - 125"
	![fov_125](images\Cores\craft\fov_125.png)	

- **Draw distance** (**10**/11/12/13/14/15/16/17/18/19/20/21/22/23/24/25/26/27/28/29/30/31/32/9/8/7/6/5/4/3/2/1): Configure the draw distance.

??? note "Draw distance - 10"
	![draw_distance_10](images\Cores\craft\draw_distance_10.png)
	
??? note "Draw distance - 32"
	![draw_distance_32](images\Cores\craft\draw_distance_32.png)
	
- **Inverted aim** (**Off**/On): Invert up and down crosshair aiming controls for the RetroPad and the RetroMouse.
- **Right analog sensitivity** (**0.0150**/0.0175/0.0200/0.0225/0.0250/0.0275/0.0300/0.0325/0.0350/0.0375/0.0400/0.0425/0.0450/0.0475/0.0500): Modify the RetroPad right analog stick's sensitivity.
- **Analog deadzone size** (**0.010**/0.015/0.020/0.025/0.030/0.035/0.040/0.045/0.050/0.055/0.060/0.065/0.070/0.075/0.080/0.085/0.090/0.095/0.100/0.110/0.115/0.120/0.125/0.130/0.135/0.140/0.145/0.150/0.155/0.160/0.165/0.170/0.175/0.180/0.185/0.190/0.195/0.200): Modify RetroPad analog sticks' deadzone.

## Controllers

*The Craft core supports the following controller setting(s), bolded controller settings are the default for the specified user(s):*

### User 1 - 16 Device Type(s)

* **RetroPad** - Joypad

* RetroPad w/Analog - Joypad - **There is no reason to switch to this.**

### Controllers graph

| Craft                | RetroPad                                                            |
|----------------------|---------------------------------------------------------------------|
| Jump                 | ![RetroPad_B](images/RetroPad/Retro_B_Round.png)                    |
| Destroy block        | ![RetroPad_Y](images/RetroPad/Retro_Y_Round.png)                    |
| Zoom out             | ![RetroPad_Select](images/RetroPad/Retro_Select.png)                |
| Move forwards        | ![RetroPad_Dpad](images/RetroPad/Retro_Dpad_Up.png)                 |
| Move backwards       | ![RetroPad_Dpad](images/RetroPad/Retro_Dpad_Down.png)               |
| Move crosshair left  | ![RetroPad_Dpad](images/RetroPad/Retro_Dpad_Left.png)               |
| Move crosshair right | ![RetroPad_Dpad](images/RetroPad/Retro_Dpad_Right.png)              |
| Next block           | ![RetroPad_A](images/RetroPad/Retro_A_Round.png)                    |
| Place block          | ![RetroPad_X](images/RetroPad/Retro_X_Round.png)                    |
| Move left            | ![RetroPad_L1](images/RetroPad/Retro_L1.png)                        |
| Move right           | ![RetroPad_R1](images/RetroPad/Retro_R1.png)                        |
| Move crosshair up    | ![RetroPad_L2](images/RetroPad/Retro_L2_Temp.png)                   |
| Move crosshair down  | ![RetroPad_R2](images/RetroPad/Retro_R2.png)                        |
| Move                 | ![RetroPad_Left_Stick](images/RetroPad/Retro_Left_Stick.png)        |
| Move crosshair       | ![RetroPad_Right_Stick](images/RetroPad/Retro_Right_Stick.png)      |

| RetroKeyboard                                                                                          | Craft                |
|--------------------------------------------------------------------------------------------------------|----------------------|
| ![Retro_Keyboard_Arrow_Up](images\Button_Pack\Keyboard_&_Mouse\Dark\Keyboard_Black_Arrow_Up.png)       | Move forward         |
| ![Retro_Keyboard_Arrow_Down](images\Button_Pack\Keyboard_&_Mouse\Dark\Keyboard_Black_Arrow_Down.png)   | Move backwards       |
| ![Retro_Keyboard_Arrow_Left](images\Button_Pack\Keyboard_&_Mouse\Dark\Keyboard_Black_Arrow_Left.png)   | Move crosshair left  |
| ![Retro_Keyboard_Arrow_Right](images\Button_Pack\Keyboard_&_Mouse\Dark\Keyboard_Black_Arrow_Right.png) | Move crosshair right |
| ![Retro_Keyboard_Right_Shift](images\Button_Pack\Keyboard_&_Mouse\Dark\Keyboard_Black_Shift_Alt.png)   | Zoom out             |

| RetroMouse                                                      | Craft          |
|-----------------------------------------------------------------|----------------|
| ![Retro_Mouse](images/RetroMouse/Retro_Mouse.png)               | Move crosshair |
| ![Retro_Left](images/RetroMouse/Retro_Left.png)                 | Destroy block  |
| ![Retro_Middle](images/RetroMouse/Retro_Middle.png)             | Copy block     |
| ![Retro_Right](images/RetroMouse/Retro_Right.png)               | Place block    |

## External Links

* [Libretro Repository](https://github.com/libretro/craft)
* [Report Core Issues Here](https://github.com/libretro/libretro-meta)
* [Official Website](https://www.michaelfogleman.com/projects/craft/)
* [Official Repository](https://github.com/fogleman/Craft)