# Board1 / PCB1 bill of materials

This is a readable view of the [original EasyEDA BOM export](../hardware/BOM_Board1_PCB1_2026-11-14.csv), dated November 14, 2026. The original file uses tabs even though its extension is `.csv`. Verify current part availability and the actual footprint before ordering.

**17 BOM rows; 20 total placements.**

| Designator | Quantity | Comment | Value | Manufacturer Part | Supplier Part |
| --- | --- | --- | --- | --- | --- |
| 3.5MM | 1 | PJ-307N5 |  | PJ-307N5 | C692542 |
| C5 | 1 | 10uF | 10uF | RD1E106M05011BB15P | C19712075 |
| DSUB1 | 1 | DS1038-15FBNSiA74-0CC |  | DS1038-15FBNSiA74-0CC | C75754 |
| L1 | 1 | RH3.5x0.8x9P52E |  | RH3.5x0.8x9P52E | C192455 |
| LED1 | 1 | TLHG4200 |  | TLHG4200 | C6333075 |
| LEFT | 1 | RCJ-042 |  | RCJ-042 | C4992825 |
| PB | 1 | RCJ-042 |  | RCJ-042 | C4992698 |
| PR,RIGHT | 2 | RCJ-042 |  | RCJ-042 | C4991949 |
| PS2 | 1 | MD-40SM |  | MD-40SM | C6212927 |
| R3 | 1 | 470Ω | 470Ω | MFR0W4F4700A50 | C58592 |
| R4 | 1 | 2.2kΩ | 2.2kΩ | RN16T22201F | C172526 |
| R5,R6 | 2 | 5.1kΩ | 5.1kΩ | MF1/8W-5.1KΩ±1% T | C119195 |
| R(C)1,R(C)2 | 2 | 100nF | 100nF | C322C104M1R5TA | C1622885 |
| U1 | 1 | LM1881N |  | LM1881N | C518923 |
| U2 | 1 | MF-R010 |  | MF-R010 | C89660 |
| USB1 | 1 | TYPEC-306DDW-ARP16 |  | TYPEC-306DDW-ARP16 | C2840393 |
| Y/CV | 1 | RCJ-042 |  | RCJ-042 | C4991830 |

The exported designators `R(C)1` and `R(C)2` refer to 100 nF capacitors. Several RCA jacks have the same manufacturer part name but distinct supplier part numbers in this export; the table preserves each one.

The [pick-and-place workbook](../hardware/PickAndPlace_PCB1_2026_11_14.xlsx) lists the positions and rotations of all 20 parts. Its `SMD` field is `No` for every placement.

