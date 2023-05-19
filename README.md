# IOkFly-Race-AM32-4in1-ESC
4in1 ESC based on AM32 FW. Developed for quad racing.

# Features

Uses AM32 open sourced 32-bit ESC FW
 * Excellent performance, excellent support and excellent community. https://github.com/AlkaMotors/AM32-MultiRotor-ESC-firmware.git

No mounting through holes
 * Allows for optimal layout to ensure a direct power flow path to each mosfet.
 * Mounting to frames is achieved with 3D printed customizable and replaceable brackets. Top and bottom in any combination of 20x20 or 30.5x30.5 mm.

Split board design
 * Allows to separate all logic components and traces from main power planes for optimal layout of components and somewhat reduces EMI.
 * Reduced heat buildup on sensitive logic components.
 * Allows for uncompromised power plane layers on PDB to achieve excellent power delivery performance.

2 Oz copper on all 6 layers of power distribution board
 * Improves current flow.
 * Improves heat distribution and heat capacity.
 * Improves shock durability.

High performance Infineon mosfets.
 * In racing power deficit is not an option.
 * IRFH7004TRPBF - https://www.infineon.com/dgdl/irfh7004pbf.pdf?fileId=5546d462533600a40153561ea3e51ed2

No current sensor
 * Current sensor and its components take a lot of valuable board space and add small power flow restriction while in racing is almost never used. Best part is no part.

FR4 Tg155 board material
 * Higher temperature tolerance and better manufacturing quality.

TDK low ESR filtering caps on the main voltage
 * High quality filtering capacitors reduce noise spikes on main power voltage and increase ESC longevity.

# Specification
 * Voltage: 4-6S
 * Current: ?>40A
 * MCU - GD32E230G6U6TR
 * Gate driver - FD6288Q
 * Mosfet - IRFH7004TRPBF
 * Target: AM32_SKYSTARS_KM55_E230
 * Mounting: 30.5x30.5 or 20x20 M3 bottoms and 30.5x30.5 or 20x20 tops with M2 or M3
 * Dimensions: 38.1x38.7x12mm
 * Weight: 17g with mount


