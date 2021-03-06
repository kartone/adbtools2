# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](http://keepachangelog.com/en/1.0.0/)
and this project adheres to [Semantic Versioning](http://semver.org/spec/v2.0.0.html).

## [v0.86] - 2018-09-25

### Changed

* [hack-script] fixed the bug that prevented loading of unsigned
  firmware if it was based on an older firmware version than the
  current one

## [v0.85] - 2018-09-25

### Changed

* [confedit] fixed the upgrade/downgrade bug appeared with the
  firmware DVA-5592_A1_WI_20180823.sig: now it is possible to enable
  upgrade/downgrade also in this release

## [v0.84]

### Added

* .exe files recompiled from python scripts and version number increased

## [v0.83]

### Added

* [confedit] added support to language translation and Italian language
* [python scripts] added Italian language

## [v0.82] - 2018-08-26

### Added

* [confedit] in the router info section added "Restricted CLI enabled" and its status

* [confedit] in the router info section added "Fix dlinkdns -> dlinkddns" and its status

* [confedit] rearranged the router info section:

   * moved "Router Customer ID" after "Model Name"
   * moved "Router IP" after "Serial Number"
   * moved "Router Netmask" after "Router IP"
   * moved "Firmware Upgrade Allowed" after "Restricted CLI commands enabled"
   * moved "Firmware Downgrade Allowed" after "Firmware Upgrade Allowed"


## [v0.81] - 2018-08-21

### Added

* [confedit] It is possible to store the preference file in the
  program folder, the default remains the user's home directory or
  APPDATA in Windows

## [v0.8] - 2018-08-19

### Added

* [mod-kit] possibility to remove files before the creation of the jffs2 image
  of the new root file system, with `root-rm-files.txt`

* [mod-kit] possibility to specify a root password, to `mod-kit-run.sh`, to be
  included in the jffs2 image of the new root file system

### Changed

* [mod-kit] default root password changed from not needed to "**no.wordpass**"
(changed file `root-patch/etc/passwd.orig.patch`)

## [v0.7] - 2018-08-16

### First release

The software is fully functional but with some limitations that could
be removed in future releases:

* [mod-kit] only the DVA-5592_A1_WI_20180405.sig firmware can be modified
  (firmware for the device D-Link DVA-5592 distributed in Italy by
  Wind and released on 2018/04/05)

* [mod-kit] new root file system image, incorporating custom modifications, must
  not be greater than current root file system image size
