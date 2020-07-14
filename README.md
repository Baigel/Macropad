This project is modified from Mattia Dal Ben's YamPad with a few changes that suit my specific needs (credit: https://github.com/mattdibi/yampad)

The Yampad project is an open-source, [QMK (Quantum Mechanical Keyboard Firmware)](https://github.com/qmk/qmk_firmware) powered, hot-swappable, RGB-backlighted, OLED featured, mechanical numpad.

## Primary Modifications from Original YamPad
 - Added 2 more switches for an array of 4x5 buttons (no more 2u keys)
 - Added spot for an IR sensor
 - Made the unused pins more accessible
 - Redid the PCB design (basically designed the PCB from scratch, loosely following Mattia Dal Ben's design)
 - idk yet, still working on it

## YamPad Features:
- Cheap to build: the PCB can be manufactured for less than 1$ per piece.
- Easy to source components.
- Easy to build.
- Hot swappable keys using *Kailh PCB sockets*.
- Arduino Pro Micro powered.
- QMK compatible.
- RGB backlighting support (optional).
- OLED 0.91" screen (optional).
- Completely open-source.

## Bill of materials

| Qty | Item                                 | Notes                                     |
|-----|--------------------------------------|-------------------------------------------|
| 1   | Arduino Pro Micro (ATmega32u4)       | a.k.a. SparkFun Pro Micro                 |
| 18  | Cherry MX compatible swtiches        |                                           |
| 18  | SOD-123 1N4148/1N4148W diodes        |                                           |
| 18  | Kailh PCB sockets CPG151101S11       |                                           |
| 9   | WS2812B RGB LEDs                     |                                           |
| 9   | SMD 0805 100nF capacitors            |                                           |
| 1   | I2C 0.91" 128*32 OLED Display Module | The ones using SSD1306 driver IC over I2C |
| 1   | 6mm*6mm button switch                |                                           |
| 1   | YamPAD/Macropad PCB                  |                                           |
| 5   | M3 screws                            |                                           |

## Assembly guide

Not necessary to assemble in this order. More details can be found on the official YamPad repository (https://github.com/mattdibi/yampad).

1. Start with soldering the **WS2812 LEDs**. Start by applying solder to a pad, then heat it up while adding the component, finally solder the remaining pads.
2. Now add the **0805 100nF caps**. Use the same technique as before.
3. Add the **1N4148 diodes**.
4. Add the **CPG151101S11 Kailh PCB sockets**.
5. Add the **reset 6mm button switch**.
6. Add some electrical tape just to be sure.
7. Add the **Arduino Pro Micro** bottom side up.
8. Add the **OLED screen**
9. Move to the firmware section and you should be set!

## Firmware

For now the firmware is available through mattdibi's [QMK firmware repository fork](https://github.com/mattdibi/qmk_firmware/tree/yampad).
```
