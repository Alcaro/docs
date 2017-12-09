# PlayStation (PCSX ReARMed)

## Contribute to this documentation

In order to propose improvements to this document, [visit its corresponding source page on github](https://github.com/libretro/docs/tree/master/docs/library/pcsx_rearmed.md). Changes are proposed using "Pull Requests."

## Background

PCSX ReARMed is a fork of PCSX Reloaded. It differs from the latter in that it has special optimizations for systems that have an ARM architecture-based CPU. It also has a dedicated graphics plugin, 'Exophase NEON GPU'. It is a surprisingly accurate graphics rasterizer that also has the ability of rendering internally in high resolution at playable framerates on ARM hardware. 

### Why use this core?

Awaiting description.

### How to get and install the PCSX ReARMed core:

1. Start up RetroArch. Inside the main menu, go to 'Online Updater'.

2. Just to make sure we have the latest info files, select 'Update Core Info FIles'. Wait until this is done. Then, select 'Core Updater'.

3. Browse through the list and select 'PlayStation (PCSX ReARMed)'.

After this has finished downloading, the core should now be ready for use!

#### How to play (after installation):

1. Go back to RetroArch's main menu screen. Select 'Load Content'.

2. Browse to the folder that contains the content you want to run.

3. Select the content that you want to run.

4. If you are asked which core to select, choose 'PlayStation (PCSX ReARMed)'.

The game should now start running!

### Authors

- PCSX Team
- notaz
- Exophase

## See also

- [PlayStation (Beetle PSX HW)](https://docs.libretro.com/library/beetle_psx_hw/) - Shared platforms.
- [PlayStation (Beetle PSX)](https://docs.libretro.com/library/beetle_psx/) - Shared platforms.

## License

A summary of the licenses behind RetroArch and its cores have found [here](https://docs.libretro.com/tech/licenses/).

- [GPLv2](https://github.com/libretro/pcsx_rearmed/blob/master/COPYING)

## Extensions

Content that can be loaded by the PCSX ReARMed core have the following file extensions:

- .bin
- .cue
- .img
- .mdf
- .pbp
- .toc
- .cbn
- .m3u

## Databases

RetroArch database(s) that are associated with the PCSX ReARMed core:

- [Sony - PlayStation](https://github.com/libretro/libretro-database/blob/master/rdb/Sony%20-%20PlayStation.rdb)

## BIOS

Required or optional firmware files go in RetroArch's system directory.

|   Filename    |    Description         |              md5sum              |
|:-------------:|:----------------------:|:--------------------------------:|
| scph5500.bin  | PS1 JP BIOS - Optional | 8dd7d5296a650fac7319bce665a6a53c |
| scph5501.bin  | PS1 US BIOS - Optional | 490f666e1afb15b7362b406ed1cea246 |
| scph5502.bin  | PS1 EU BIOS - Optional | 32736f17079d0b2b7024407c39bd3050 |

!!! warning
	In case the PCSX ReARMed can find no BIOS files named like this in RetroArch's system directory, it will default to a High-Level Emulation BIOS. This decreases the level of compatibility of the emulator, so it is recommended that you always supply valid BIOS images inside the system directory. 

## Features

| Feature           | Supported |
|-------------------|:---------:|
| Restart           | ✔         |
| Screenshots       | ✔         |
| Saves             | ✔         |
| States            | ✔         |
| Rewind            | ✔         |
| Netplay           | ✔         |
| Core Options      | ✔         |
| RetroAchievements | ✕         |
| RetroArch Cheats  | ✔         |
| Native Cheats     | ✕         |
| Controls          | ✔         |
| Remapping         | ✔         |
| Multi-Mouse       | ✕         |
| Rumble            | ✔         |
| Sensors           | ✕         |
| Camera            | ✕         |
| Location          | ✕         |
| Subsystem         | ✕         |
| Softpatching      | ✕         |
| Disk Control      | ✔         |
| Username          | ✕         |
| Crop Overscan     | ✕         |

### Saves/States

The PCSX ReARMed core's directory name is 'PCSX-ReARMed'

Game data is saved/loaded to and from where save files are stored.

- .srm (Memory card slot 0)

Save states are saved/loaded to and from where state files are stored.

- .state (State)

### Core provided aspect ratio

PCSX ReARMed's core provided aspect ratio is 4/3.

### Loading content

PCSX ReARMed needs a cue-sheet that points to an image file. A cue sheet, or cue file, is a metadata file which describes how the tracks of a CD or DVD are laid out.

If you have e.g. `foo.bin`, you should create a text file and save it as `foo.cue`. Most PS1 games are single-track, so the cue file contents should look like this:

`foobin.cue`
```
 FILE "foo.bin" BINARY
  TRACK 01 MODE1/2352
   INDEX 01 00:00:00
```

After that, you can load the `foo.cue` file in RetroArch with the PCSX ReARMed core.

!!! warning ""
    Certain PS1 games are multi-track, so their .cue files might be more complicated.
	
#### Playing PAL copy protected games

PAL copy protected games need a SBI Subchannel file next to the bin/cue files in order to get past the copy protection.

- Ape Escape (Europe).bin
- Ape Escape (Europe).cue
- **Ape Escape (Europe).sbi**

#### Multiple-disk games

If foo is a multiple-disk game, you should have .cue files for each one, e.g. `foo (Disc 1).cue`, `foo (Disc 2).cue`, `foo (Disc 3).cue`.

To take advantage of PCSX ReARMed's Disk Control feature for disk swapping, an index file (a m3u file) should be made.

Create a text file and save it as `foo.m3u`. Then enter your game's .cue files on it. The m3u file contents should look something like this:

`foo.m3u`
```
foo (Disc 1).cue
foo (Disc 2).cue
foo (Disc 3).cue
```

After that, you can load the `foo.m3u` file in RetroArch with the PCSX ReARMed core.

Here's another m3u example done with Valkryie Profile

![m3u_example](images\Cores\beetle_psx_hw\m3u_example.png)

!!! warning ""
	Adding multi-track games to a RetroArch playlist is recommended. (Manually add an entry a playlist that points to `foo.m3u`)

#### Game compression

Alternatively to using cue sheets with .bin files, you can convert your games to .pbp (Playstation Portable update file) to reduce file sizes and neaten up your game folder. A recommended .pbp convert tool is PSX2PSP.

If converting a multiple-disk game, all disks should be added to the same .pbp file, rather than making a .m3u file for them.

Most conversion tools will want a single .bin file for each disk. If your game uses multiple .bin files (tracks) per disk, you will have to mount the cue sheet to a virtual drive and re-burn the images onto a single track before conversion.

!!! warning ""
    RetroArch does not currently have .pbp database due to variability in users' conversion methods. All .pbp games will have to be added to playlists manually.

### Saves

For game savedata storage, the PSX console used memory cards. The PSX console had two slots for memory cards.

The PCSX ReARMed core only has support for the first memory card slot.

In this doc, the first memory card slot will be referred to as 'Memcard slot 0'.

For memory card functionality and usage, the PCSX ReARMed core will the Libretro savedata format.

<center>

| Libretro savedata format   |
|----------------------------|
| gamename.srm               |

</center>

**By default**, the filename of the Memcard savedata will match the loaded cue or m3u or pbp filename, like this:

- Loaded content: Breath of Fire III (USA).cue

- **Memcard slot 0: Breath of Fire III (USA).srm**

or

- Loaded content: Final Fantasy VII (USA).m3u

- **Memcard slot 0: Final Fantasy VII (USA).srm**

or

- Loaded content: Wild Arms 2 (USA).pbp

- **Memcard slot 0: `Wild Arms 2 (USA).srm**

!!! warning ""
	To import your old memory cards from other emulators, you need to rename them to the Libretro savedata format.

### Rumble

Rumble only works when the 'Enable Vibration' core option is set to On and the joypad input driver being used has rumble function implementation (e.g. **Xinput**).

## Core options

The PCSX ReARMed core has the following option(s) that can be tweaked from the core options menu. The default setting is bolded.

- **Frameskip** (**0**/1/2/3)

<center> Choose how much frames should be skipped to improve performance at the expense of visual smoothness. </center>

- **Region** (**Auto**/NTSC/PAL)

<center> Choose what region the system is from. </center>

- **Pad 1 Type** (**default**/none/standard/analog/negcon)

<center> Choose the Pad Type for User 1. </center>

<center> With the none setting, input is disabled. </center>

<center> With the standard setting, a standard [PlayStation Controller](https://en.wikipedia.org/wiki/PlayStation_Controller) is emulated. </center>

<center> With the analog setting, a [Dual Analog Controller](https://en.wikipedia.org/wiki/Dual_Analog_Controller) is emulated </center>

<center> With the negcon setting, a [neGcon Controller](https://en.wikipedia.org/wiki/NeGcon) is emulated. </center>

<center> Check the [Controllers section](https://buildbot.libretro.com/.docs/library/pcsx_rearmed/#controllers) for more information. </center>

- **Pad 2 Type** (**default**/none/standard/analog/negcon)

<center> Choose the Pad Type for User 2. </center>

<center> With the none setting, input is disabled. </center>

<center> With the standard setting, a standard [PlayStation Controller](https://en.wikipedia.org/wiki/PlayStation_Controller) is emulated. </center>

<center> With the analog setting, a [Dual Analog Controller](https://en.wikipedia.org/wiki/Dual_Analog_Controller) is emulated </center>

<center> With the negcon setting, a [neGcon Controller](https://en.wikipedia.org/wiki/NeGcon) is emulated. </center>

<center> Check the [Controllers section](https://buildbot.libretro.com/.docs/library/pcsx_rearmed/#controllers) for more information. </center>

- **Pad 3 Type** (**default**/none/standard/analog/negcon) 

<center> Choose the Pad Type for User 3. </center>

<center> With the none setting, input is disabled. </center>

<center> With the standard setting, a standard [PlayStation Controller](https://en.wikipedia.org/wiki/PlayStation_Controller) is emulated. </center>

<center> With the analog setting, a [Dual Analog Controller](https://en.wikipedia.org/wiki/Dual_Analog_Controller) is emulated </center>

<center> With the negcon setting, a [neGcon Controller](https://en.wikipedia.org/wiki/NeGcon) is emulated. </center>

<center> Check the [Controllers section](https://buildbot.libretro.com/.docs/library/pcsx_rearmed/#controllers) for more information. </center>

- **Pad 4 Type** (**default**/none/standard/analog/negcon)
 
<center> Choose the Pad Type for User 4. </center>

<center> With the none setting, input is disabled. </center>

<center> With the standard setting, a standard [PlayStation Controller](https://en.wikipedia.org/wiki/PlayStation_Controller) is emulated. </center>

<center> With the analog setting, a [Dual Analog Controller](https://en.wikipedia.org/wiki/Dual_Analog_Controller) is emulated </center>

<center> With the negcon setting, a [neGcon Controller](https://en.wikipedia.org/wiki/NeGcon) is emulated. </center>

<center> Check the [Controllers section](https://buildbot.libretro.com/.docs/library/pcsx_rearmed/#controllers) for more information. </center>

- **Pad 5 Type** (**default**/none/standard/analog/negcon)

<center> Choose the Pad Type for User 5. </center>

<center> With the none setting, input is disabled. </center>

<center> With the standard setting, a standard [PlayStation Controller](https://en.wikipedia.org/wiki/PlayStation_Controller) is emulated. </center>

<center> With the analog setting, a [Dual Analog Controller](https://en.wikipedia.org/wiki/Dual_Analog_Controller) is emulated </center>

<center> With the negcon setting, a [neGcon Controller](https://en.wikipedia.org/wiki/NeGcon) is emulated. </center>

<center> Check the [Controllers section](https://buildbot.libretro.com/.docs/library/pcsx_rearmed/#controllers) for more information. </center>

- **Pad 6 Type** (**default**/none/standard/analog/negcon)

<center> Choose the Pad Type for User 6. </center>

<center> With the none setting, input is disabled. </center>

<center> With the standard setting, a standard [PlayStation Controller](https://en.wikipedia.org/wiki/PlayStation_Controller) is emulated. </center>

<center> With the analog setting, a [Dual Analog Controller](https://en.wikipedia.org/wiki/Dual_Analog_Controller) is emulated </center>

<center> With the negcon setting, a [neGcon Controller](https://en.wikipedia.org/wiki/NeGcon) is emulated. </center>

<center> Check the [Controllers section](https://buildbot.libretro.com/.docs/library/pcsx_rearmed/#controllers) for more information. </center>

- **Pad 7 Type** (**default**/none/standard/analog/negcon)

<center> Choose the Pad Type for User 7. </center>

<center> With the none setting, input is disabled. </center>

<center> With the standard setting, a standard [PlayStation Controller](https://en.wikipedia.org/wiki/PlayStation_Controller) is emulated. </center>

<center> With the analog setting, a [Dual Analog Controller](https://en.wikipedia.org/wiki/Dual_Analog_Controller) is emulated </center>

<center> With the negcon setting, a [neGcon Controller](https://en.wikipedia.org/wiki/NeGcon) is emulated. </center>

<center> Check the [Controllers section](https://buildbot.libretro.com/.docs/library/pcsx_rearmed/#controllers) for more information. </center>

- **Pad 8 Type** (**default**/none/standard/analog/negcon)

<center> Choose the Pad Type for User 8. </center>

<center> With the none setting, input is disabled. </center>

<center> With the standard setting, a standard [PlayStation Controller](https://en.wikipedia.org/wiki/PlayStation_Controller) is emulated. </center>

<center> With the analog setting, a [Dual Analog Controller](https://en.wikipedia.org/wiki/Dual_Analog_Controller) is emulated </center>

<center> With the negcon setting, a [neGcon Controller](https://en.wikipedia.org/wiki/NeGcon) is emulated. </center>

<center> Check the [Controllers section](https://buildbot.libretro.com/.docs/library/pcsx_rearmed/#controllers) for more information. </center>
 
- **Multitap 1** (**auto**/Off/On)
 
<center> Enables/Disables [multitap](https://en.wikipedia.org/wiki/PlayStation_Multitap) functionality on port 1, allowing 3-8 player support in games that permit it. </center>

- **Multitap 2** (**auto**/Off/On)

<center> Enables/Disables [multitap](https://en.wikipedia.org/wiki/PlayStation_Multitap) functionality on port 2, allowing 3-8 player support in games that permit it. </center>

- **Enable Vibration** (Off/**On**)

<center> Enables Rumble. Look at the [Rumble section](https://buildbot.libretro.com/.docs/library/pcsx_rearmed/#rumble) for more information </center>

- **Enable Dithering** (Off/**On**)

<center> If Off, disables the dithering pattern the PSX applies to combat color banding. </center>

<center>

??? note "Enable Dithering - On"
	![](images\Cores\pcsx_rearmed\dither_on.png)
	
</center>
	
<center>
	
??? note "Enable Dithering - Off"
	![](images\Cores\pcsx_rearmed\dither_off.png)
	
</center>	

- **Frame duping** (Off/**On**)

<center> A speedup, redraws/reuses the last frame if there was no new data. </center>

- **Show Bios Bootlogo(Breaks some games)** (**Off**/On)

<center> Self explanatory. </center>

- **Sound: Reverb** (Off/**On**)

<center> Awaiting description. </center>

- **Sound: Interpolation** (**simple**/gaussian/cubic/off)

<center> Awaiting description. </center>

- **Parasite Eve 2/Vandal Hearts 1/2 Fix** (**Off**/On)

<center> Self explanatory. </center>

- **InuYasha Sengoku Battle Fix** (**Off**/On)

<center> Self explanatory. </center>

## Controllers

### Device types

The PCSX ReARMed core supports the following device type(s) in the controls menu, bolded device types are the default for the specified user(s):

#### User 1 - 8 device types

- **RetroPad** - Joypad
- **RetroPad w/Analog** - Joypad - **There is no reason to switch to this.**

### Controller tables

#### Joypad and analog device type table

| User 1 - 8 input descriptors  |                                              | standard    | analog         | negcon |
|-------------------------------|----------------------------------------------|-------------|----------------|--------|
| Cross                         | ![](images/RetroPad/Retro_B_Round.png)       | Cross       | Cross          | -      |
| Square                        | ![](images/RetroPad/Retro_Y_Round.png)       | Square      | Square         | -      |
| Select                        | ![](images/RetroPad/Retro_Select.png)        | Select      | Select         | -      |
| Start                         | ![](images/RetroPad/Retro_Start.png)         | Start       | Start          | -      |
| D-Pad Up                      | ![](images/RetroPad/Retro_Dpad_Up.png)       | D-Pad Up    | D-Pad Up       | -      |
| D-Pad Down                    | ![](images/RetroPad/Retro_Dpad_Down.png)     | D-Pad Down  | D-Pad Down     | -      |
| D-Pad Left                    | ![](images/RetroPad/Retro_Dpad_Left.png)     | D-Pad Left  | D-Pad Left     | -      |
| D-Pad Right                   | ![](images/RetroPad/Retro_Dpad_Right.png)    | D-Pad Right | D-Pad Right    | -      |
| Circle                        | ![](images/RetroPad/Retro_A_Round.png)       | Circle      | Circle         | -      |
| Triangle                      | ![](images/RetroPad/Retro_X_Round.png)       | Triangle    | Triangle       | -      |
| L1                            | ![](images/RetroPad/Retro_L1.png)            | L1          | L1             | -      |
| R1                            | ![](images/RetroPad/Retro_R1.png)            | R1          | R1             | -      |
| L2                            | ![](images/RetroPad/Retro_L2.png)            | L2          | L2             | -      |
| R2                            | ![](images/RetroPad/Retro_R2.png)            | R2          | R2             | -      |
| L3                            | ![](images/RetroPad/Retro_L3.png)            |             | L3             | -      |
| R3                            | ![](images/RetroPad/Retro_R3.png)            |             | R3             | -      |
| Left Analog X                 | ![](images/RetroPad/Retro_Left_Stick.png) X  |             | Left Analog X  | -      |
| Left Analog Y                 | ![](images/RetroPad/Retro_Left_Stick.png) Y  |             | Left Analog Y  | -      |
| Right Analog X                | ![](images/RetroPad/Retro_Right_Stick.png) X |             | Right Analog X | -      |
| Right Analog Y                | ![](images/RetroPad/Retro_Right_Stick.png) Y |             | Right Analog Y | -      |

## Compatibility

| Game            | Issue                                                  |
|-----------------|--------------------------------------------------------|
| Jumping Flash 2 | Graphics glitches. Geometry issues.                    |
| Tobal 2         | Graphics glitch. Garbled Dream Factory intro sequence. |

## External Links

- [Libretro PCSX ReARMed Core info file](https://github.com/libretro/libretro-super/blob/master/dist/info/pcsx_rearmed_libretro.info)
- [Libretro PCSX ReARMed Github Repository](https://github.com/libretro/pcsx_rearmed)
- [Report Libretro PCSX ReARMed Core Issues Here](https://github.com/libretro/pcsx_rearmed/issues)
- [Official PCSX ReARMed Website](http://notaz.gp2x.de/pcsx_rearmed.php)
- [Official PCSX ReARMed Github Repository](https://github.com/notaz/pcsx_rearmed)
