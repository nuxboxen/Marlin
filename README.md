![Banner Image](https://imgur.com/1A545RY.png)
#               Choose a Path 

**PATH 1.** I've downloaded a couple .zip files from Github
    before but otherwise it just looks like shit I
    don't have an interest in, I just want to flash my
    SKR MiniE3 V2 that works with my EZABL and get the
    hell away from all this elite developer garbage.
    Give me a file!!!
**PATH 2.** I think it would be cool to get my hands on all the source
    files for Marlin and have a good base setup for my
    EZABL, maybe even make a few tweeks to the config 
    files myself and then compile the source into a binary
    myself.  This isn't that big of a deal but could you
    explain a little more about exactly what you've got
    going on here Nux.
**PATH 3.** Linus Torvalds takes coding lessongs from me and all 
   of you incel 3d printer people need to RTFM how dare
   you even visit github you don't even know what a repo is...



#             PATH 1  (GIVE ME THE .BIN FILE!)

Ok ok,  all you need to do is download the .zip file from
the page you are currently on.  Scroll up a little and find
the Green Button that says "Code" click the button and choose
the bottom option "Download ZIP"  and save that zip file
like you would any other downloaded file.   Open the zip and
move SKR-EZABL-firmware.bin to your printers SDCard and rename
it to firmware.bin.  Insert SDCard in you printer, power up and 
the printer will replace it's firmware with the one you just added
by itself.  

*Note: If on first boot you see an error about EEPROM not matching
that is not a problem.  Use the menu to reset to "factory defaults"
(don't worry it's just clearing a few settings from your old setup)
then choose "store settings" and the EEprom is ready to go.*

You're up and running the new firmware now:  you can finish setting
up the probe offsets, I recomment the video below for a good guide
to all the steps you'll need to do after the firmware flash, just
ignore their firmware flashing it doesn't work with the skr boards.
[*Skip to 19:40* The Edge Of Tech EZABL howto](https://www.youtube.com/watch?v=8dYBvPl6wkU)

Please Realise:  Because this is a .bin file you've downloaded
                 and flashed you are stuck with alot of choices 
                 that I made for you.  There are still lots of
                 options you can set through m codes and the
                 control menus but some of the deeper options 
                 of the firmware can't be changed at this point.
                 If you need to do some of those type of changes
                 you're going to have to follow path 2 and 
                 complile a .bin yourself.

#             PATH 2  (LET'S COMPILE A BIN FILE!!!)             

**So What Is This All About:**I'm going to use a little git terminology the name of this repository is "nuxboxen/Marlin' which is a "fork" of "MarlinFirmware/Marlin"
that means it's a copy of the official Marlin firware source code for a person who
is not part of the development team to do with as they like.  In this case
all I'm doing is making changes in the configuration files and the README.md
to allow for the use of the EZABL with the SKRMini E3 V2 board which is
not documented well.

**Branches:** Marlin has several "branches" of the code, just think of each branch as a
seperate copy that is in a different state of change then the other "branches"
If you scroll back up this page you'll see a button that has a branch symbol
and "2.0.x"  What that button is telling you is that you are currently on the
"2.0.x branch"  here's the thing that's not the branch we want to be using
we wan't to use "bugfix-2.0x".  I put the precompiled .bin and this README.md 
in this "2.0.x branch" to keep it simple for people on Path 1.   
the file you are reading README.md will actually change to a different page
because that branch is a completely different copy of the files.  **So to find
the rest of the directions switch the branch to "bugfix-2.0.x" and you'll
find a README.md with the rest of the directions for PATH 2.**  See you there...


#             PATH 3  (I'M WAY SMARTER THEN YOU NUX)

Hey congratulations on your achievments in life, sorry this project seems
so elementary but it works.  If we ever cross paths I'll buy you lunch and
have a hundred questions for you.

          


![GitHub](https://img.shields.io/github/license/marlinfirmware/marlin.svg)
![GitHub contributors](https://img.shields.io/github/contributors/marlinfirmware/marlin.svg)
![GitHub Release Date](https://img.shields.io/github/release-date/marlinfirmware/marlin.svg)
[![Build Status](https://github.com/MarlinFirmware/Marlin/workflows/CI/badge.svg?branch=bugfix-2.0.x)](https://github.com/MarlinFirmware/Marlin/actions)

<img align="right" width=175 src="buildroot/share/pixmaps/logo/marlin-250.png" />

Additional documentation can be found at the [Marlin Home Page](http://marlinfw.org/).
Please let us know if Marlin misbehaves in any way. Volunteers are standing by!

## Marlin 2.0

Marlin 2.0 takes this popular RepRap firmware to the next level by adding support for much faster 32-bit and ARM-based boards while improving support for 8-bit AVR boards. Read about Marlin's decision to use a "Hardware Abstraction Layer" below.

Download earlier versions of Marlin on the [Releases page](https://github.com/MarlinFirmware/Marlin/releases).

## Building Marlin 2.0

To build Marlin 2.0 you'll need [Arduino IDE 1.8.8 or newer](https://www.arduino.cc/en/main/software) or [PlatformIO](http://docs.platformio.org/en/latest/ide.html#platformio-ide). Detailed build and install instructions are posted at:

  - [Installing Marlin (Arduino)](http://marlinfw.org/docs/basics/install_arduino.html)
  - [Installing Marlin (VSCode)](http://marlinfw.org/docs/basics/install_platformio_vscode.html).

### Supported Platforms

  Platform|MCU|Example Boards
  --------|---|-------
  [Arduino AVR](https://www.arduino.cc/)|ATmega|RAMPS, Melzi, RAMBo
  [Teensy++ 2.0](http://www.microchip.com/wwwproducts/en/AT90USB1286)|AT90USB1286|Printrboard
  [Arduino Due](https://www.arduino.cc/en/Guide/ArduinoDue)|SAM3X8E|RAMPS-FD, RADDS, RAMPS4DUE
  [LPC1768](http://www.nxp.com/products/microcontrollers-and-processors/arm-based-processors-and-mcus/lpc-cortex-m-mcus/lpc1700-cortex-m3/512kb-flash-64kb-sram-ethernet-usb-lqfp100-package:LPC1768FBD100)|ARM® Cortex-M3|MKS SBASE, Re-ARM, Selena Compact
  [LPC1769](https://www.nxp.com/products/processors-and-microcontrollers/arm-microcontrollers/general-purpose-mcus/lpc1700-cortex-m3/512kb-flash-64kb-sram-ethernet-usb-lqfp100-package:LPC1769FBD100)|ARM® Cortex-M3|Smoothieboard, Azteeg X5 mini, TH3D EZBoard
  [STM32F103](https://www.st.com/en/microcontrollers-microprocessors/stm32f103.html)|ARM® Cortex-M3|Malyan M200, GTM32 Pro, MKS Robin, BTT SKR Mini
  [STM32F401](https://www.st.com/en/microcontrollers-microprocessors/stm32f401.html)|ARM® Cortex-M4|ARMED, Rumba32, SKR Pro, Lerdge, FYSETC S6
  [STM32F7x6](https://www.st.com/en/microcontrollers-microprocessors/stm32f7x6.html)|ARM® Cortex-M7|The Borg, RemRam V1
  [SAMD51P20A](https://www.adafruit.com/product/4064)|ARM® Cortex-M4|Adafruit Grand Central M4
  [Teensy 3.5](https://www.pjrc.com/store/teensy35.html)|ARM® Cortex-M4|
  [Teensy 3.6](https://www.pjrc.com/store/teensy36.html)|ARM® Cortex-M4|

## Submitting Changes

- Submit **Bug Fixes** as Pull Requests to the ([bugfix-2.0.x](https://github.com/MarlinFirmware/Marlin/tree/bugfix-2.0.x)) branch.
- Follow the [Coding Standards](http://marlinfw.org/docs/development/coding_standards.html) to gain points with the maintainers.
- Please submit your questions and concerns to the [Issue Queue](https://github.com/MarlinFirmware/Marlin/issues).

## Marlin Support

For best results getting help with configuration and troubleshooting, please use the following resources:

- [Marlin Documentation](http://marlinfw.org) - Official Marlin documentation
- [Marlin Discord](https://discord.gg/n5NJ59y) - Discuss issues with Marlin users and developers
- Facebook Group ["Marlin Firmware"](https://www.facebook.com/groups/1049718498464482/)
- RepRap.org [Marlin Forum](http://forums.reprap.org/list.php?415)
- [Tom's 3D Forums](https://discuss.toms3d.org/)
- Facebook Group ["Marlin Firmware for 3D Printers"](https://www.facebook.com/groups/3Dtechtalk/)
- [Marlin Configuration](https://www.youtube.com/results?search_query=marlin+configuration) on YouTube

## Credits

The current Marlin dev team consists of:

 - Scott Lahteine [[@thinkyhead](https://github.com/thinkyhead)] - USA &nbsp; [Donate](http://www.thinkyhead.com/donate-to-marlin) / Flattr: [![Flattr Scott](http://api.flattr.com/button/flattr-badge-large.png)](https://flattr.com/submit/auto?user_id=thinkyhead&url=https://github.com/MarlinFirmware/Marlin&title=Marlin&language=&tags=github&category=software)
 - Roxanne Neufeld [[@Roxy-3D](https://github.com/Roxy-3D)] - USA
 - Chris Pepper [[@p3p](https://github.com/p3p)] - UK
 - Bob Kuhn [[@Bob-the-Kuhn](https://github.com/Bob-the-Kuhn)] - USA
 - João Brazio [[@jbrazio](https://github.com/jbrazio)] - Portugal
 - Erik van der Zalm [[@ErikZalm](https://github.com/ErikZalm)] - Netherlands &nbsp; [![Flattr Erik](http://api.flattr.com/button/flattr-badge-large.png)](https://flattr.com/submit/auto?user_id=ErikZalm&url=https://github.com/MarlinFirmware/Marlin&title=Marlin&language=&tags=github&category=software)

## License

Marlin is published under the [GPL license](/LICENSE) because we believe in open development. The GPL comes with both rights and obligations. Whether you use Marlin firmware as the driver for your open or closed-source product, you must keep Marlin open, and you must provide your compatible Marlin source code to end users upon request. The most straightforward way to comply with the Marlin license is to make a fork of Marlin on Github, perform your modifications, and direct users to your modified fork.

While we can't prevent the use of this code in products (3D printers, CNC, etc.) that are closed source or crippled by a patent, we would prefer that you choose another firmware or, better yet, make your own.
