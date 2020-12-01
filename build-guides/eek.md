---
layout: default
title: eek! Docs
parent: Build Guides
---

# eek! Documentation and links:
---
## eek! links:
- [klackygears case files, docs, and firmware](https://github.com/Klackygears/eek_doc)

## Assembling the eek!

The eek! follows the normal rules when assembling the board. Below is an example of how the diodes, LEDs, and MX switches should be soldered. Keep in mind that if you flip the board to show the bat and eek! silk up, these same rules apply. 

![eek_bat](https://i.imgur.com/YrOqmft.jpeg)


The footprints for the diodes have a small arrow indicating whitch direction the black line (or white line with SMD diodes).

![diode_footprint](https://raw.githubusercontent.com/Klackygears/eek_case/main/Photos/footprint_diode.jpg)

The LED order is below. Like Christmas lights, if you have a problem with one of the LEDs all of the LEDs after will not work.

![LED_order](https://raw.githubusercontent.com/Klackygears/eek_case/main/Photos/LED_order.JPG)


The SK6812 MINI E (be sure to get the **"E"** type) have one leg that has a clipped angle. That angled leg should be placed on the pad with the outline.

![LED_footprint](https://raw.githubusercontent.com/Klackygears/eek_case/main/Photos/footprint_LED.jpg)


The eek! is compatible with MX, ALPs, and Choc style switches. In the first image below, be careful not to bridge solder across the red lines. Depending on your configuration, you may connect the column and rows so that the switch always appears to be pressed. This will cause strange problems. In the second image below, the colored dots represent the switch legs in the footprint: Red for MX, Green for ALPs, Blue for Choc. 

1)
![switch_footprint](https://raw.githubusercontent.com/Klackygears/eek_case/main/Photos/footprint_switch.jpg)

2)
![switchtypes_footprint](https://raw.githubusercontent.com/Klackygears/eek_case/main/Photos/footprint_switch_types.jpg)


The Pro Micro (or clone) should be soldered to the pcb on the side with the gear logo as seen in the picture below. If you are using a variant with castilated holes, the pads on eek! support soldering the Pro Micro on that way for a low profile build. **_Regardless if you decide to have the pcb flipped or not, the pro micro should be installed the same way._** 

**I recommend flashing firmware on the pro micro before soldering to make sure that it's working properly.**

![ProMicro_orientation](https://raw.githubusercontent.com/Klackygears/eek_case/main/Photos/ProMicro_placement2.jpg)


## Flashing the eek!

Once you have your build environment set up using the guide in the **[QMK Documentation](https://docs.qmk.fm/)** I recommend flashing the eek! with the default keymap or the ledtest keymap to make sure that everything is soldered correctly. 

QMK firmware github is [here](https://github.com/qmk/qmk_firmware).

QMK eek specific will be [here](https://github.com/qmk/qmk_firmware).

If you made the eek! with the bat silk side down use the command:

``make eek:default``

If you made the eek! with the bat silk side up use the command:

``make eek/silk_up:default``


Disclaimer: Though it may be tempting, eek! is not a snack.
