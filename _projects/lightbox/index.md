---
layout: post
title: One Shot Blinking Lightbox
description:  Designed and built an Arduino-based lightbox system, developing custom firmware, PCB schematics, and a 3D-printed enclosure that integrated LEDs, MOSFET drivers, sensors, and user controls.
skills: 
- KiCad
- Onshape
- 3D Printing
- C++
- Python
- Arduino Firmware
main-image: /oneshot.png
---

---
## CAD Design
Enclosure of the lightbox:
{% include image-gallery.html images="Enclosure_base_walls.png" height="400" %} 
<br>
PCB Mounts for the base of the enclosure:
{% include image-gallery.html images="Mounts.png" height="400" %} 

## PCB Design
Schematic:
{% include image-gallery.html images="schematic.png" height="400" %} 
PCB:
{% include image-gallery.html images="pcb.png" height="400" %} 

## Component Footprints

| Description | Part Number | Digikey Part Number |
| --- | --- | --- |
| Arduino Nano Every | ABX00033 | 1050-ABX00033-ND |
| Push Button | PS1024ALRED | EG2025-ND |
| Toggle Switch | SW-T3-1A-A-A3-S1 | 2057-SW-T3-1A-A-A3-S1-ND |
| LED | PM5RD | 492-1659-ND |
| 15 Pin Header | PPTC151LFBN-RC | S7013-ND |
| 9V Battery | ZEUS 9V | 2059-ZEUS9V-ND |
| Battery Connector | 232 | 36-232-ND |
| 2 Pin Connector | B02B-XASK-1 | 455-B02B-XASK-1-ND |
| 3 Pin Connector | B03B-XASK-1 | 455-B03B-XASK-1-ND |
| 2 Pin Jumper | A02XAF02XAF22K152B | 455-3061-ND |
| 3 Pin Jumper | A03KR03KR26E152B | 455-3379-ND |
| 10k Potentiometer | PDB181-E420K-103B | PDB181-E420K-103B-ND |
| Transistor | IRFZ44 | (TO220 Packaging) |

## Firmware 

- SPST push button switch (ON/OFF) to turn "eye" LEDs on for 5 seconds and
"nose" LED for 10 seconds.

- Potentiometer to adjust brightness of "eye" LEDs using PWM (0-100%).

- Potentiometer to adjust blinking rate of "nose" LED (5-10 Hz).

- Have the on-board NanoEvery LED act as a "heartbeat" LED blinking at 1 Hz in all states.
