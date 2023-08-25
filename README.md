# chocofi temper

This is a split, wireless-only mechanical keyboard fashioned after the [chocofi keyboard](https://github.com/pashutk/chocofi). It started as a simple modification of the original chocofi PCBs to include battery pads and power switches for wireless use, but in the end, I thought there were enough changes to warrant giving it a separate designation. However, this design remains compatible with chocofi cases and plates.

## Features

- 36-key split keyboard with 3 rows x 5 columns + 3 thumb keys per half 
- Kailh choc spacing
- Sweep-like column stagger (with pinky columns 2 mm lower, like chocofi) with Corne-like thumb cluster
- Reversible PCB (so one design can be used for both halves)
- Kailh choc hotswap sockets
- Intended to be used with [nice!nano](https://nicekeyboards.com/nice-nano)
- Uses 7-pin SPDT power switch and includes pads for battery on keyboard shield PCB
- Support for [nice!view](https://nicekeyboards.com/nice-view), though this hasn't been tested yet
- Compatible with chocofi cases and plates

## List of changes from original chocofi

- Add power switch
- Add solder pads for battery under ProMicro footprint
- Add footprint for a nice!view screen
- Switch out diode footprints for ones that have solder pads on both sides
- Switch ProMicro footprint for one that uses solder jumpers for cleaner design
- Remove TRRS jack
- Change reset switch out for one I could easily source from [Typeractive](https://www.typeractive.xyz)
- Rework KiCAD schematic for more pleasant development

## Bill of Materials

- PCB x2
- 2x nice!nanos
- 2x LiPo batteries (see nice!nano documentation for suggestions)
- 2x Alps miniature SPDT switches
- 2x Panasonic miniature momentary button switches 
- 36x Kailh choc v1 switches
- 36x Kailh choc hotswap sockets
- 36x Choc v1 keycaps
- 36x 1N4148W SMD diodes
- (Optional) 4x Mill-Max 310 series machine sockets + 48x Mill-Max pins for socketing microcontrollers
- (Optional) 2x nice!view screens

## Firmware

This keyboard uses [ZMK firmware](https://zmk.dev), which allows for configuration through GitHub Actions. An example configuration repository is [here](https://github.com/raeedcho/temper-zmk-config.git).

## Why "temper"?

Tempering is a finicky process that changes the structure of chocolate to make it more shiny, but doesn't really change the taste much.

Likewise, the changes I made to the chocofi didn't alter the original design much, but made some quality-of-life improvements for both development and my own personal aesthetics, at the cost of removing traditional wired operation and possibly making it more difficult to assemble, given the addition of many solder jumpers. 

## Resources

I adapted a few of the elements from these KiCAD libraries for use in this design:

- [chocofi](https://github.com/pashutk/chocofi) - The PCB switch layout came from the original chocofi design
- [kbd](https://github.com/foostan/kbd) - This library, by foostan, the designer of the popular Corne keyboard, provides useful schematic symbols and footprints
- [keyswitches.pretty](https://github.com/daprice/keyswitches.pretty) - library of switch footprints--especially useful for reversible PCBs.
- [swoop](https://github.com/jimmerricks/swoop) - Contains reversible PCB footprints for ProMicro pinout, OLED screens, and 7-pin power switches.


## Similar keyboards

There are many similar keyboards to this one and the chocofi, and I'm sure they've all taken inspiration from each other at one point or another. Here's a (surely incomplete) list:

- [Corne/crkbd](https://github.com/foostan/crkbd) - A popular column stagger, 42-key split keyboard with many variants
- [Cornish Zen](https://lowprokb.ca/collections/keyboards/products/corne-ish-zen) - A low-profile wireless redesign of the Corne with choc spacing, screens, and an aluminum case
- [Kyria](https://splitkb.com/collections/keyboard-kits/products/kyria-rev3-pcb-kit) - Another popular columns stagger, 50-key split keyboard, supporting rotary encoders. MX spacing only, but supports both MX and choc switches. More extreme column stagger on the pinky than the Corne. Large thumb cluster.
- [Ferris](https://github.com/pierrechevalier83/ferris) - Minimalistic 34-key split keyboard borrowing the pinky column stagger of the Kyria. MCU is soldered directly onto the board--not ProMicro pinout compatible.
- [Ferris Sweep](https://github.com/davidphilipbarr/Sweep) - Redesign of the Ferris for ProMicro MCU pinout, which also allows for a diodeless build. Many variations.
- [Swoop](https://github.com/jimmerricks/swoop) - Fork of the Ferris Sweep to add OLED screens and encoders
- [Urchin](https://github.com/duckyb/urchin) - Another fork of the Ferris Sweep to add support for nice!view screens, though with a traditional switch matrix and diodes.
- [Swept Corne](https://github.com/AYM1607/swept-crkbd) - A wireless-only mix between the Corne and Ferris Sweep--basically a choc-spaced Corne with the Kyria pinky stagger (or alternatively a choc-spaced Kyria with a Corne thumb cluster)
- [Phase](https://github.com/mjpauly/phase) - 42-key split keyboard--mix of the original Ferris and Corne.
- [Fifi](https://github.com/raychengy/fifi_split_keeb) - 36-key split keyboard. Basically an MX Ferris Sweep with a Corne thumb cluster
- [Chocofi](https://github.com/pashutk/chocofi) - Choc version of the Fifi. Stagger is like the Kyria and Ferris keyboards, but with the pinky column 2mm lower. The keyboard this repository was based on.
- [Roost](https://github.com/forrestbaer/roost) - Wireless-only Ferris Sweep with an extra thumb key per hand
- [TOTEM](https://github.com/GEIGEIGEIST/TOTEM) - 38 key split keyboard with Sweep-like column stagger. 3 thumb keys, like Corne, but also an extra pinky key. Also designed with finger splay for the ring and pinky fingers.
- [A. Dux](https://github.com/tapioki/cephalopoda/tree/main/Architeuthis%20dux) - 34-key split keyboard with aggressive column stagger and splay
- [KLOR](https://github.com/GEIGEIGEIST/KLOR) - Customizable split keyboard (via versatile break-off PCBs), with on-board MCU, encoders, and OLED screens
