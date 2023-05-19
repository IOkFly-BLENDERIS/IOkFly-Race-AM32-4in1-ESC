# IOkFly-Race-AM32-4in1-ESC

<p align="left">
  <a href="/LICENSE.md"><img src="https://img.shields.io/badge/License-CC_BY--NC--SA_4.0-lightgrey.svg" alt="GitHub license" /></a>
</p>


4in1 ESC based on [AM32 FW](https://github.com/AlkaMotors/AM32-MultiRotor-ESC-firmware.git). Every commercial  ESC on the market has some sort of design compromise to satisfy as many use cases as possible. My plan was to develop uncompromised, performance oriented ESC for quadcopter racing. Combining all of the features mentioned below I believe that I achieved to design a perfect ESC for racing.

# Features

Uses AM32 open sourced 32-bit ESC FW
 * Excellent performance, excellent support and excellent community.

No mounting through holes
 * Allows for optimal layout to ensure a direct power flow path to each mosfet.
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
 * [IRFH7004TRPBF](https://www.infineon.com/dgdl/irfh7004pbf.pdf?fileId=5546d462533600a40153561ea3e51ed2)

No current sensor
 * Current sensor and its components take a lot of valuable board space and add small power flow restriction while in racing is almost never used. Best part is no part.

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

![ESC pinout](https://github.com/IOkFly-BLENDERIS/IOkFly-Race-AM32-4in1-ESC/assets/133950976/bc576cc6-4df9-4c56-b795-eccb09293f3f) ![Processing board](https://github.com/IOkFly-BLENDERIS/IOkFly-Race-AM32-4in1-ESC/assets/133950976/73a3530e-2c1e-4727-bb3a-f7e3f9611904)


# Manufacuring
I used [EasyEDA](https://easyeda.com/) (free PCB design tool) for designing the boards. [LCS](https://www.lcsc.com/) for ordering components and [JLCPCB](https://jlcpcb.com/) for manufacuring the boards as well as assembling the processing board. Processing board has allot of 0201 components and it is almost impossible to assemble a DIY way.

PCB manufacturing specification:

PDB:
 * Layers: 6
 * Base Material: FR4 Tg155
 * PCB Thickness: 1.6mm
 * Inner Copper Weight: 2oz
 * Outer Copper Weight: 2oz
 * Via Covering: Epoxy Filled & Capped
 * Surface Finish: ENIG Gold Thickness:2 U"
 * Castellated Holes: yes, Edges: 4
 
 Processing Board:
  * Layers: 6
  * Base Material: FR4 Tg140
  * PCB Thickness: 0.8mm
  * Inner Copper Weight: 0.5oz
  * Outer Copper Weight: 1oz
  * Via Covering: Epoxy Filled & Capped
  * Surface Finish: ENIG Gold Thickness:1 U"
  * Castellated Holes: yes, Edges: 4

For assembling the ESC I use solder paste with stencil from JLCPCB. Alignment of Processing board on the PCB is critical as the Processing board has very tightly spaced and small castellated holes. Bad alignment may result in shorts or cold soldering. Heat gun soldering or reflow oven will require long and high heat profiles as the PCB has huge termal capacity. I used cheap soldering heat gun on max temp settings with medium tip for about 5 minutes per side.

![WhatsApp attēls 2023-05-19 plkst  23 57 41](https://github.com/IOkFly-BLENDERIS/IOkFly-Race-AM32-4in1-ESC/assets/133950976/46544f7f-2648-4b49-8de7-97c145edd307) ![WhatsApp attēls 2023-05-19 plkst  23 58 39](https://github.com/IOkFly-BLENDERIS/IOkFly-Race-AM32-4in1-ESC/assets/133950976/137dd823-da13-488f-b00a-537decf66462)\
![WhatsApp attēls 2023-05-20 plkst  00 01 37](https://github.com/IOkFly-BLENDERIS/IOkFly-Race-AM32-4in1-ESC/assets/133950976/daaf9efb-222e-439d-98ae-7d41ca2b58da) ![WhatsApp attēls 2023-05-20 plkst  00 01 06](https://github.com/IOkFly-BLENDERIS/IOkFly-Race-AM32-4in1-ESC/assets/133950976/b8cb1636-6c32-4a70-8240-b06e4d07a260)





# Testing

Flight testing:
https://www.youtube.com/watch?v=bb6y31JhEbI \
Current draw testing: Coming soon...

# Contributors

Pete Smits\
Jurģis Punculis\
AM32 Discord coumunity


