# JOST Launcher for kickstart 1.3
Game/Demo launcher for JOST exe to run .slave for WHDLOAD compatible with 1.3 kickstart

This is kind of a clone of [TinyLauncher](https://aminet.net/package/util/misc/TinyLauncher) from "Master" Gibs (french will understand this stupid joke).

The target setup for this launcher is a CDTV with 8Mo fast memory and BlueCDTV/BlueSCSI SD Card hard disk.

You can fully control the launcher with your CDTV Remote, mouse mode or joy mode.

: ![screenshot](screen_v0.2.png)

# How to setup

Prequisites :
- You need `jost` in your `C:` folder. [Download](https://github.com/jotd666/jst)
- Kickstarts files. Legit files can be bought from [Amiga Forever](https://www.amigaforever.com/)

1. Copy `jl` executable n your `C:` folder.
2. Change content and copy `jl-config.cfg` to `S:` folder
3. Launch jl and launch a scan. It should add a `jl-inventory.data` in your `S:` folder

Launch it through CLI or add it in your startup sequence.

# How to control

CDTV Remote (mouse mode or joy mode) :
- Arrow to navigate
- A or B button To launch
- 0 to scan your whdload games or demo folder.
- 1 to switch to folder mode
- Escape to quite

Any joystick/joypad :
- Arrow to navigate
- A or B button To launch

Keyboard :
- Arrow to navigate
- Enter button To launch
- S to scan your whdload games or demo folder.
- Escape to quite
- F to switch to folder mode

# jl-config.cfg setup

## scan_dir_1

**Mandatory**

To specify the folder to be scanned. No trailing `/` at the end please.

Example:

`scan_dir_1=Games:Games`

## inventory_file

_Optional_

To specify an inventory file other than the default one (`S:jl-inventory.data`)

Example:

`inventory_file=Games:inventory_1.data`

## folder_mode_by_default

_Optional_

TO define default behaviour after startup (folder mode or list mode).

`folder_mode_by_default=true`


# Dev Documentation

- http://amigadev.elowar.com/read/ADCD_2.1/Includes_and_Autodocs_3._guide/node015E.html
- https://github.com/jotd666/jst

# Credits

 - Jotd/Jean-François Fabre for his huge work on jst.
 - Daedalus and Earok from the blitzbasic.dev discord.
 - Whdload contributors.
 - Gibs for his work on TinyLauncher.

# Release Notes

## 0.3
 - feat: folder view mode
 - refactor: display info
 - feat: display current JL version
 - feat: new optional config entry `folder_mode_by_default`
 - fix: display refresh before and after scan

## 0.2
 - feat: Add alphabetical order on games display
 - fix: hardcoded limit of 100 games
 - fix: Scan on 1.3 not working on more than the 1st folder
 - feat: new optional config entry `inventory_file`

## 0.1
 - Initial alpha version
  
# Dev packaging

Lha command :
`lha a jl.lha jl README.md jl-config.cfg`