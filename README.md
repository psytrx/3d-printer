# 3d-printer

My printer setup, print profiles and Klipper config. Breaking changes regularly happen (due to firmware updates and major Klipper releases), so versioning is crucial to me.

## Setup

I'm printing on a direct drive modified Ender 3 in an IKEA Lack enclosure. It's running Klipper (Fluidd) on a Raspberry Pi.

## Hardware mods

Most significant modifications include:

- BTT SKR 1.2 Mini E3 1.3 MCU
- **TMC2209 UART** drivers for less noise
- **E3D Hemera** direct drive for higher flow and more accurate extrusions
- **BL Touch** clone for z homing and fewer bed leveling
- **Glass bed** for better adhesion

## Klipper config

`printer.cfg` is the full Klipper config file for my setup. The config includes:

- Basic pin setup for the steppers, extruder, heaters and fans
- Screw tilt adjust config for the default Ender 3 bed size
- Safe homing

- Temperature sensors for Raspberry Pi and MCU
- Input Shaper (**warning**: This will definitely vary for your config, no matter the same hardware setup)
- GCode macros for `PAUSE`, `RESUME`, `G29` and `CANCEL_PRINT`
