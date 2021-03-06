# Atari 8-bit computer systems and 5200 (Atari800)

## Contribute to this documentation

In order to propose improvements to this document, [visit its corresponding source page on github](https://github.com/libretro/docs/tree/master/docs/library/atari800.md). Changes are proposed using "Pull Requests."

## Background

Atari 8-bit computer systems (400, 800, 600 XL, 800XL, 130XE) and 5200 game console emulator.

### How to get and install the Atari800 core:

1. Start up RetroArch. Inside the main menu, go to 'Online Updater'.

2. Just to make sure we have the latest info files, select 'Update Core Info FIles'. Wait until this is done. Then, select 'Core Updater'.

3. Browse through the list and select 'Atari 8-bit computer systems and 5200 (Atari800)'.

After this has finished downloading, the core should now be ready for use!

#### How to play (after installation):

1. Go back to RetroArch's main menu screen. Select 'Load Content'.

2. Browse to the folder that contains the content you want to run.

3. Select the content that you want to run.

4. If you are asked which core to select, choose 'Atari 8-bit computer systems and 5200 (Atari800)'.

The game should now start running!

### Authors

- Petr Stehlik

## See also

Awaiting description.

## License

A summary of the licenses behind RetroArch and its cores have found [here](https://docs.libretro.com/tech/licenses/).

- [GPLv2](https://github.com/atari800/atari800/blob/master/COPYING)

## Extensions

Content that can be loaded by the Atari800 core have the following file extensions:

- .xfd
- .atr
- .atx
- .cdm
- .cas
- .bin
- .a52
- .xex
- .zip

## Databases

RetroArch database(s) that are associated with the Atari800 core:

- [Atari - 5200](https://github.com/libretro/libretro-database/blob/master/rdb/Atari%20-%205200.rdb)

## BIOS

Required or optional firmware files go in RetroArch's system directory.

|   Filename    |    Description                         |              md5sum              |
|:-------------:|:--------------------------------------:|:--------------------------------:|
| 5200.rom      | 5200 BIOS - Required                   | 281f20ea4320404ec820fb7ec0693b38 |
| ATARIXL.ROM   | Atari XL/XE OS BIOS - Required         | 06daac977823773a3eea3422fd26a703 |
| ATARIBAS.ROM  | BASIC interpreter BIOS - Required      | 0bac0c6a50104045d902df4503a4c30b |
| ATARIOSA.ROM  | Atari 400/800 PAL BIOS - Required      | eb1f32f5d9f382db1bbfb8d7f9cb343a |
| ATARIOSB.ROM  | BIOS for Atari 400/800 NTSC - Required | a3e8d617c95d08031fe1b20d541434b2 |

## Features

| Feature           | Supported |
|-------------------|:---------:|
| Restart           | ✕         |
| Screenshots       | ✔         |
| Saves             | -         |
| States            | -         |
| Rewind            | ✕         |
| Netplay           | ✕         |
| Core Options      | ✔         |
| RetroAchievements | ✕         |
| RetroArch Cheats  | ✕         |
| Native Cheats     | -         |
| Controls          | ✔         |
| Remapping         | ✔         |
| Multi-Mouse       | ✕         |
| Rumble            | ✕         |
| Sensors           | ✕         |
| Camera            | ✕         |
| Location          | ✕         |
| Subsystem         | ✕         |
| Softpatching      | ✕         |
| Disk Control      | ✕         |
| Username          | ✕         |
| Crop Overscan (in RetroArch's Video settings) | ✕         |

### Directories

The Atari800 core's directory name is 'Atari800'

Atari800 config settings are saved/loaded to and from .atari800.cfg in RetroArch's home directory (where RetroArch.exe is in Windows).

- .atari800.cfg (Config)

### Core provided aspect ratio

Atari800's core provided aspect ratio is 4/3.

### Usage

Make sure you have the appropriate system files in RetroArch's system directory. Then, load a content file.

The Atari800 core should boot to the 'Atari Computer - Memo Pad' screen.

The Atari800 core will generate a '.atari800.cfg' config file in RetroArch's home directory and will add the required BIOS files it detects in the system directory to the config file.

Now you can manually select what Atari system you want to emulate through the 'Atari System' core option.

Finally, you can load any content files compatible with the system chosen through RetroArch's Load Content menu.

!!! attention
	You can set per-game core option settings by creating a game-options file through RetroArch's Core Opitons menu.

Alternatively, you can manually configure how the Atari800 will look for and handle BIOS files.

While the Atari800 core is running, you can press F1 to get into the internal emulator menu. There - emulator configuration, system rom settings.

From there, You can go to the 'Emulator Configuration' section and then the System ROM settings section to configure BIOS options. (Press Enter to confirm menu selections and press Escape to go back a menu)

Then press Escape a few times to go back to the 'Emulator Configuration' section and select Save Configuration File or alternatively change Save configuration file on exit from no to yes

Then you can exit the emulator by pressing F9 and then try the game again or press Shift+F5 to reboot the game.

## Core options

The Atari800 core has the following option(s) that can be tweaked from the core options menu. The default setting is bolded. Settings with (Restart) means that core has to be closed for the new setting to be applied on next launch.

- **Atari System** (**400/800 (OS B)**/800XL (64K)/130XE (128K)/5200)

<center> Choose what Atari System to emulate. </center>

- **Video Standard** (**NTSC**/PAL)

<center> Awaiting description. </center>

- **Internal BASIC (hold OPTION on boot)** (**Off**/On)

<center> Awaiting description. </center>

- **SIO Acceleration** (**Off**/On)

<center> Awaiting description. </center>

- **Boot from Cassette** (**Off**/On)

<center> Awaiting description. </center>

- **Hi-Res Artifacting** (**Off**/On)

<center> Awaiting description. </center>

- **Autodetect A5200 CartType** (**Off**/On)

<center> Awaiting description. </center>

- **Joy hack A5200 for robotron** (**Off**/On)

<center> Awaiting description. </center>

- **Internal resolution** (**336x240**/320x240/384x240/384x272/384x288/400x300)

<center> Awaiting description. </center>

- **Retroarch Keyboard type** (**poll**/callback)

<center> Awaiting description. </center>

## Controllers

### Device types

The Atari800 core supports the following device type(s) in the controls menu, bolded device types are the default for the specified user(s):

#### User 1 - 2 device types

- None - Input disabled.
- **RetroPad** - Joypad - Don't use this, switch to ATARI Joystick for joypad usage.
- ATARI Joystick - Joypad
- ATARI Keyboard - Keyboard - For keyboard usage

### Controller tables

#### Joypad and analog device type table

| User 1 input descriptors      |                                              | ATARI Joystick          |
|-------------------------------|----------------------------------------------|-------------------------|
| B                             | ![](images/RetroPad/Retro_B_Round.png)       | KEY RETURN              |
| Y                             | ![](images/RetroPad/Retro_Y_Round.png)       | VKBD ON/OFF             |
| Select                        | ![](images/RetroPad/Retro_Select.png)        | CONSOL_SELECT           |
| Start                         | ![](images/RetroPad/Retro_Start.png)         | CONSOL_START            |
| Up                            | ![](images/RetroPad/Retro_Dpad_Up.png)       | Up                      |
| Down                          | ![](images/RetroPad/Retro_Dpad_Down.png)     | Down                    |
| Left                          | ![](images/RetroPad/Retro_Dpad_Left.png)     | Left                    |
| Right                         | ![](images/RetroPad/Retro_Dpad_Right.png)    | Right                   |
| A                             | ![](images/RetroPad/Retro_A_Round.png)       | FIRE1/KEY RETURN IN GUI |
| X                             | ![](images/RetroPad/Retro_X_Round.png)       | FIRE2/KEY ESCAPE IN GUI |
| L                             | ![](images/RetroPad/Retro_L1.png)            | CONSOL_OPTION           |
| R                             | ![](images/RetroPad/Retro_R1.png)            | TOGGLE UI               |
| L2                            | ![](images/RetroPad/Retro_L2.png)            | KEY SPACE               |
| R2                            | ![](images/RetroPad/Retro_R2.png)            | KEY ESCAPE              |
| L3                            | ![](images/RetroPad/Retro_L3.png)            | N/A                     |
| R3                            | ![](images/RetroPad/Retro_R3.png)            | N/A                     |

#### Keyboard device type table

| User # input descriptors      |                               | ATARI Keyboard             |
|-------------------------------|-------------------------------|----------------------------|
| N/A                           | Keyboard Numpad 2             | Down                       |
| N/A                           | Keyboard Numpad 4             | Left                       |
| N/A                           | Keyboard Numpad 6             | Right                      |
| N/A                           | Keyboard Numpad 8             | Up                         |
| N/A                           | Keyboard Up                   | Up                         |
| N/A                           | Keyboard Down                 | Down                       |
| N/A                           | Keyboard Right                | Right                      |
| N/A                           | Keyboard Left                 | Left                       |
| N/A                           | Keyboard F1                   | Built in UI                |
| N/A                           | Keyboard F2                   | Option key                 |
| N/A                           | Keyboard F3                   | Select key                 |
| N/A                           | Keyboard F4                   | Start key                  |
| N/A                           | Keyboard F5                   | Reset key                  |
| N/A                           | Keyboard F6                   | Help key (XL/XE only)      |
| N/A                           | Keyboard F7                   | Break key                  |
| N/A                           | Keyboard F8                   | Enter monitor              |
| N/A                           | Keyboard F9                   | Exit emulator              |
| N/A                           | Keyboard F10                  | Save screenshot            |
| N/A                           | Keyboard Right Control        | Fire                       |
| N/A                           | Keyboard Shift + F5           | Reboot                     |
| N/A                           | Keyboard Shift + F10          | Save interlaced screenshot |
| N/A                           | Keyboard Alt + R              | Run Atari program          |
| N/A                           | Keyboard Alt + D              | Disk management            |
| N/A                           | Keyboard Alt + C              | Cartridge management       |
| N/A                           | Keyboard Alt + Y              | Select system              |
| N/A                           | Keyboard Alt + O              | Sound settings             |
| N/A                           | Keyboard Alt + W              | Sound recording start/stop |
| N/A                           | Keyboard Alt + S              | Save state file            |
| N/A                           | Keyboard Alt + L              | Load state file            |
| N/A                           | Keyboard Alt + A              | About the emulator         |

## External Links

- [Libretro Atari800 Core info file](https://github.com/libretro/libretro-super/blob/master/dist/info/atari800_libretro.info)
- [Libretro Atari800 Github Repository](https://github.com/libretro/libretro-atari800)
- [Report Libretro Atari800 Core Issues Here](https://github.com/libretro/libretro-atari800/issues)
- [Official Atari800 Website](https://atari800.github.io/)
- [Official Atari800 Github Repository](https://github.com/atari800/atari800)