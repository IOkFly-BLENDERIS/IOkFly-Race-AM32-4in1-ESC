# IOkFly-Race-AM32-4in1-ESC

<p align="left">
  <a href="/LICENSE.md"><img src="https://img.shields.io/badge/License-CC_BY--NC--SA_4.0-lightgrey.svg" alt="GitHub license" /></a>
</p>


4in1 ESC based on [AM32 FW](https://github.com/AlkaMotors/AM32-MultiRotor-ESC-firmware.git). Every commercial ESC on the market has some sort of design compromise to satisfy as many use cases as possible. My plan was to develop uncompromised, performance oriented ESC for quadcopter racing. Combining all the features mentioned below I believe that I achieved to design a perfect ESC for racing.

# Features

Uses AM32 open sourced 32-bit ESC FW
 * Excellent performance, excellent support and excellent community.

No mounting through holes
 * Allows for optimal mosfet layout to ensure a direct power flow path to each mosfet.
 * Mounting to frames is achieved with 3D printed customizable and replaceable brackets. Top and bottom in any combination of 20x20 or 30.5x30.5 mm.

Split board design
 * Allows to separate all logic components and traces from main power planes for optimal layout of components and somewhat reduces EMI.
 * Reduced heat buildup on sensitive logic components.
 * Allows for uncompromised power plane layers on PDB to achieve excellent power delivery performance.

2 oz copper weight on all 6 layers of power distribution board
 * Improves current flow.
 * Improves heat distribution and heat capacity.
 * Improves shock durability.

High performance Infineon mosfets.
 * In racing power deficit is not an option.
 * IRFH7004TRPBF](https://www.infineon.com/dgdl/irfh7004pbf.pdf?fileId=5546d462533600a40153561ea3e51ed2)

No current sensor
 * Current sensor and its components use valuable board space and adds a small power flow restriction while in racing it`s almost never used. Best part is no part. There are external XT60 current sensor boards available if needed.\
![Ekrānuzņēmums 2023-05-21 213739](https://github.com/IOkFly-BLENDERIS/IOkFly-Race-AM32-4in1-ESC/assets/133950976/2d17819c-baca-40b2-acc5-546fded5815f)

FR4 Tg155 board material
 * Higher temperature tolerance and better manufacturing quality.

TDK low ESR filtering caps on the main voltage
 * High quality filtering capacitors reduce noise spikes on main power voltage and increase ESC longevity.

# Specification
 * Voltage: 4-6S
 * Current: 40A < ?
 * MCU - GD32E230G6U6TR
 * Gate driver - FD6288Q
 * Mosfet - IRFH7004TRPBF
 * Target: AM32_SKYSTARS_KM55_E230
 * Mounting: 30.5x30.5 or 20x20 M3 bottoms and 30.5x30.5 or 20x20 tops with M2 or M3
 * Dimensions: 38.1x38.7x12mm
 * Weight: 17g with mount

![ESC pinout](https://github.com/IOkFly-BLENDERIS/IOkFly-Race-AM32-4in1-ESC/assets/133950976/62eea24b-0331-443b-aff9-20422fb3c1ae) ![Processing board](https://github.com/IOkFly-BLENDERIS/IOkFly-Race-AM32-4in1-ESC/assets/133950976/2936366c-c37b-44f8-91a1-f6106755df46)

# Manufacturing
I used [EasyEDA](https://easyeda.com/) (free PCB design tool) for designing the boards. [LCS](https://www.lcsc.com/) for ordering components and [JLCPCB](https://jlcpcb.com/) for manufacturing the boards as well as assembling the processing board. Processing board has a lot of 0201 components, and it is almost impossible to assemble in a DIY way.

PCB manufacturing and assembling:

PDB specification: 
 * Layers: 6
 * Base Material: FR4 Tg155
 * PCB Thickness: 1.6mm
 * Inner Copper Weight: 2oz
 * Outer Copper Weight: 2oz
 * Via Covering: Epoxy Filled & Capped
 * Surface Finish: ENIG Gold Thickness:2 U"
 * Castellated Holes: yes, Edges: 4
 
 Processing Board specification:
  * Layers: 6
  * Base Material: FR4 Tg140
  * PCB Thickness: 0.8mm
  * Inner Copper Weight: 0.5oz
  * Outer Copper Weight: 1oz
  * Via Covering: Epoxy Filled & Capped
  * Surface Finish: ENIG Gold Thickness:1 U"
  * Castellated Holes: yes, Edges: 4

For assembling the ESC, I use solder paste with stencil from JLCPCB. Alignment of Processing board on the PCB is critical as the Processing board has very tightly spaced and small castellated holes. Bad alignment may result in shorts or cold soldering. Heat gun soldering or reflow oven will require long and high heat profiles as the PCB has huge thermal capacity. I used cheap soldering heat gun on max temperature settings with medium tip and low air flow for about 5 minutes per side.\
![WhatsApp attēls 2023-05-19 plkst  23 57 41](https://github.com/IOkFly-BLENDERIS/IOkFly-Race-AM32-4in1-ESC/assets/133950976/be19ce04-929f-4c8b-be93-1ee4f63ee6dd) ![WhatsApp attēls 2023-05-19 plkst  23 58 39](https://github.com/IOkFly-BLENDERIS/IOkFly-Race-AM32-4in1-ESC/assets/133950976/bc83deef-e31b-4360-b07a-066a26edbc2e)

#Mounting

So far, I have used only PETG material for 3D printed mounts. Works well with racing frames such as Switchback. Mounts rigidly to the frame and ESC. Bottom mount requires some sort of threaded inserts to be melted in.
\
![Ekrānuzņēmums 2023-05-22 124104](https://github.com/IOkFly-BLENDERIS/IOkFly-Race-AM32-4in1-ESC/assets/133950976/328543dc-c4b1-4d4f-8700-b02bd240db86)

Top mount takes screws directly. Top and bottom part is screwed together with M2 screws in the corners. Recommended height of the frame standoffs are 25mm.

# Testing

Flight testing:
https://www.youtube.com/watch?v=bb6y31JhEbI \
Current draw testing: Coming soon...

# Contributors

Pete Smits\
IOkFly_FluxssFPV\
AM32 Discord community

