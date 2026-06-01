# GhostCutter

A CoreXY diode laser cutter built on a 2020 aluminium extrusion frame.

## Overview

GhostCutter is a simple DIY coreXY designed laser cutter designed on a coreXY 3d printer like frame built for hotswap toolheads

## Specs

| Parameter | Value |
|-----------|-------|
| Frame | 2020 aluminium extrusion |
| Motion system | CoreXY |
| Machine footprint | 500x650mm |
| Cutting area | ~400x400mm |
| Laser module | LaserTree LT-80W-AA (10W optical) |
| Wavelength | 450nm |

## BOM

| Part | Qty | Source | Cost (USD) |
|------|-----|--------|------|
| MGN12 linear rails | 3 | on hand | $30 |
| 2020 aluminium extrusion 100mm | 6 | [Core Electronics](https://core-electronics.com.au/2020-aluminium-extrusion-600mm.html) | $70 |
| 17HS24-2104S NEMA 17 stepper motors | 2 | [OMC StepperOnline](https://www.omc-stepperonline.com/nema-17-bipolar-1-8deg-65ncm-92oz-in-2-1a-3-36v-42x42x60mm-4-wires-17hs24-2104s) | $43 |
| LaserTree LT-80W-AA laser module | 1 | [LaserTree](https://lasertree.com/products/10w-optical-output-power-laser-cutter-module) | $131 |
| Air assist pump | 1 | [Sculpfun](https://www.sculpfun.com/products/sculpfun-air-pump) | $69 |
| Misc (pulleys x10, belts, screws) | 3 | aliexpress | $30 |
| 3D printed parts | NA | print farm (on hand) | $0 |
| **Total** | | | **~$347** |

> Controller board, enclosure panels, acrylic bed slats, and safety goggles not yet costed above.

# Bed Design

The bed uses a Clear acrylic slat design. This means that it uses a diode laser's inability to cut through clear acrylic as an advantage rather than a drawback. Slats slide into a 3D printed base with shallow grooves on one side and deep grooves on the other to form a slatted bed.

### Laser Head
LT-80w-AA with a 10w Optical Output - This fits on to a hotswap head

### Electronics
TBD

### Enclosure
Laser rated acrylic

## Safety

This machine uses a Class 4 laser. Permanent eye damage can occur in milliseconds.

- Always wear wavelength-appropriate laser safety goggles (OD4+ at 450nm)
- Operate only with enclosure panels in place
- Never leave unattended during operation
- Ensure that there is ventilation

## Firmware & Software

| Component | Software |
|-----------|---------|
| Firmware | TBD |
| Slicer/CAM | Going to be custom |


## Progress Log

- [x] CAD — frame
- [x] CAD — CoreXY motion system
- [x] CAD — bed
- [x] CAD — laser head mount
- [x] CAD — enclosure
- [X] IRL — frame assembly
- [ ] IRL — motion system
- [ ] IRL — wiring & firmware
- [ ] First cut

## License

MIT

### Made by Aarav J :D
