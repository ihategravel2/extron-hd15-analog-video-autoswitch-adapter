# Board1 build and wiring notes

These notes describe the through-hole **Board1 / PCB1** export dated November 14, 2026. Use the [original BOM](../hardware/BOM_Board1_PCB1_2026-11-14.csv) for exact manufacturer and supplier parts, and inspect the [Gerber ZIP](../hardware/Gerber_PCB1_2026-11-14.zip) in a fabrication viewer before ordering.

## Signal connections

| Connector/contact | Net | Destination |
| --- | --- | --- |
| `Y/CV` RCA center | Y | HD15 pin 2 and LM1881 sync input through a 100 nF capacitor |
| `PB` RCA center | PB | HD15 pin 3 |
| `PR` RCA center | PR | HD15 pin 1 |
| `PS2` 4-pin mini-DIN pin 3 | Y | HD15 pin 2 and sync input |
| `PS2` 4-pin mini-DIN pin 4 | PR | HD15 pin 1 |
| LM1881 composite-sync output | CSYNC | HD15 pin 13 through R3 (470 Ω) |
| `LEFT` RCA center | LEFT | 3.5 mm jack left channel |
| `RIGHT` RCA center | RIGHT | 3.5 mm jack right channel |
| RCA outer contacts and mini-DIN ground pins | GND | HD15 ground pins and 3.5 mm sleeve |

The RCA Y/CV input and mini-DIN luma connection share a net, as do the RCA Pr input and mini-DIN chroma connection. Do not drive both connectors on either shared path at once.

The circuit derives sync from Y/CV. Pb and Pr are passed through to the HD15 connector without a color-space conversion stage. For composite-over-green use, feed composite video to `Y/CV`. For S-Video use, feed luma/chroma to `PS2`. Configure the receiving Extron input for the supplied format and timing.

## Power and parts

USB-C VBUS passes through the MF-R010 resettable fuse and ferrite bead to the 5 V rail. Two 5.1 kΩ USB-C CC resistors are on the board. The rail powers the LM1881 and LED indicator. The supplied BOM and pick-and-place export list **20 through-hole placements**.

Two 100 nF capacitors appear as `R(C)1` and `R(C)2` in the EasyEDA exports; they are capacitors despite those designators. Check orientation for the LED, electrolytic C5, USB-C connector, and LM1881 before soldering.

## Checks before use

1. Inspect the board outline, copper, solder mask, and both plated and non-plated drill files in the Gerber ZIP.
2. Compare the physical board markings with the BOM and placement workbook. Verify connector orientation and clearance.
3. With power disconnected, check for shorts between 5 V and ground, and check continuity on the signal routes above.
4. Apply 5 V through USB-C. Confirm the power indicator and the LM1881 supply voltage before connecting an Extron device.
5. Confirm the intended video signal appears on the mapped HD15 pins and that composite sync appears on pin 13. Then test input detection and switching on the target Extron device.

The exports do not establish compatibility with every Extron model or input configuration. Review the specific device's pinout and supported input formats before use.

