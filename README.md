# Prusa-Fast-Macros

Prusa-Fast-Macros contains the macro definitions that I personally use on my MK3S+ running Klipper.
These macros have been optimized for speed. If you run Klipper on your cartesian Prusa printer,
I'm sure you will find something useful here! These macro are for reference only.

![macros](https://github.com/8bitmcu/Prusa-Fast-Macros/blob/main/macros.png?raw=true)

## build_sheets.cfg

Contains a set of macros that I use to manage the different offsets of my build plates. Originally 
forked from [klipper-voron2.4-config](https://github.com/garethky/klipper-voron2.4-config), 
I've added a macro that let's you choose from the list of installed build plates.

## calibration.cfg

Contains a very small set of simple calibration macros, in which the Z calibration has been sped up.

## main.cfg

Contains the bulk of the useful macros.

  - `PRINT_START`: Pretty typical print start macro that isn't too picky on the bed/hotend temperature
  - `PRINT_END`: Typical print end macro that notifies me on Telegram that the print is done before clearing values that I sometimes overwrite in the slicer.
  - `CANCEL_PRINT`: Cancels the actual print and clear values.
  - `_TOOLHEAD_PARK_PAUSE_CANCEL`: Parks the toolhead, fast.
  - `CUSTOM_LINE_PURGE`: Custom extra long purge line that I'm still not entirely happy with. Nothing fast here.
  - `UNLOAD_FILAMENT`: Unloads more filament that the original macro.
  - `LOAD_FILAMENT`: Typical filament loading macro.

## marlin.cfg

Contains a subset of marlin gcode commands that aren't found in klipper. Thus being able to reprint
MK3S+ sliced files for marlin in klipper.

Also contains the `M600` macro which I've modified so it parks directly in the front and faster.


##


note: `PRINT_END`, `CANCEL_PRINT` and `M600` uses the [moonraker-telegram-bot](https://github.com/nlef/moonraker-telegram-bot) plugin.
