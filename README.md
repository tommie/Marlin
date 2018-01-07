# Marlin 3D Printer Firmware
<img align="right" src="Documentation/Logo/Marlin%20Logo%20GitHub.png" />

 Additional documentation can be found in [our wiki](https://github.com/MarlinFirmware/Marlin/wiki/Main-Page).

## Creality Ender-2 Support

This branch is a reverse-engineered version based on the unpublished firmware from Creality. It is **not** the authoritative source, but has been carefully re-built by looking at their firmware and inferring the base version and configuration they used. The basis is the firmware version from "Jul 31 2017 10:16:30". It is based on Marlin 1.0.1, because

* 1.0.0 had very different serial output in `setup()` and overall code structure.
* 1.0.2 changed the `VERSION_STRING` to include a leading space, and `lcd_init` uses `SET_INPUT` instead of `pinMode`.

Configurations were found by seeing what code was compiled into the firmware, and constants used there.

For U8Glib, at least version 1.14 and at most 1.17 is used, because

* 1.12 didn't have the extra speed argument to u8g_InitCom.
* 1.13 didn't have the soft reset instruction for UC1701 initialization.
* 1.18 has a new directory structure.

## Release Branch

The Release branch contains the latest tagged version of Marlin (currently 1.0.2-2 – October 2016). It also includes a version 1.0.1 (December 2014). Any version of Marlin before 1.0.1 (when we started tagging versions) can be collectively referred to as Marlin 1.0.0.

## Patches - 1.0.x Branch

Any patches developed for this family of releases will be found on the [1.0.x branch](https://github.com/MarlinFirmware/Marlin/tree/1.0.x) of this repository.

## This Repository is Not For Feature Development

Development of future versions of Marlin is ongoing. However, to keep issues separate, that effort takes place in a companion [Development Repository](https://github.com/MarlinFirmware/MarlinDev/). Please make all suggestions for future features in that project. Issues raised here should be restricted to errors in the tagged releases.

## Current Status: In Development

Marlin development is being accelerated to catch up with a long list of issues. Check the Issues and Pull Requests links on the right to to see what we are currently working on.

[![Coverity Scan Build Status](https://scan.coverity.com/projects/2224/badge.svg)](https://scan.coverity.com/projects/2224)
[![Travis Build Status](https://travis-ci.org/MarlinFirmware/Marlin.svg)](https://travis-ci.org/MarlinFirmware/Marlin)

##### [RepRap.org Wiki Page](http://reprap.org/wiki/Marlin)

## Credits

The current Marlin dev team consists of:

 - Scott Lahteine [@thinkyhead] - English
 - Roxanne Neufeld [@Roxy-3DPrintBoard] - English
 - Andreas Hardtung [@AnHardt] - Deutsch, English
 - [@Wurstnase] - Deutsch, English
 - [@fmalpartida] - English, Spanish
 - [@CONSULitAS] - Deutsch, English
 - [@maverikou]
 - Chris Palmer [@nophead]
 - [@paclema]
 - [@epatel]
 - Erik van der Zalm [@ErikZalm]
 - David Braam [@daid]
 - Bernhard Kubicek [@bkubicek]

More features have been added by:
  - Alberto Cotronei [@MagoKimbra]
  - Lampmaker,
  - Bradley Feldman,
  - and others...

## License

Marlin is published under the [GPL license](/COPYING.md) because we believe in open development. The GPL comes with both rights and obligations. Whether you use Marlin firmware as the driver for your open or closed-source product, you must keep Marlin open, and you must provide your compatible Marlin source code to end users upon request. The most straightforward way to comply with the Marlin license is to make a fork of Marlin on Github, perform your modifications, and direct users to your modified fork.

While we can't prevent the use of this code in products (3D printers, CNC, etc.) that are closed source or crippled by a patent, we would prefer that you choose another firmware or, better yet, make your own.

[![Flattr this git repo](http://api.flattr.com/button/flattr-badge-large.png)](https://flattr.com/submit/auto?user_id=ErikZalm&url=https://github.com/MarlinFirmware/Marlin&title=Marlin&language=&tags=github&category=software)
