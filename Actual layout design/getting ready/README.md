# CMOS Inverter Layout Preparation

Transforming a simulation-verified CMOS inverter into a fabrication-ready design for Magic VLSI.

## What Was Done

**Design & Verification**
- Designed and sized CMOS inverter (NMOS/PMOS)
- Performed transient and DC analysis
- Verified logic operation (LOW→HIGH, HIGH→LOW)

**Schematic Cleanup**
- Removed simulation-only components:
  - Voltage sources
  - Load capacitor
- Kept only fabrication elements (transistors + interconnects)

**Port Definition**

![CMOS Inverter Schematic with Ports](schematic-image.png)

| Signal | Type | Function |
|--------|------|----------|
| VIN | Input | Signal input |
| VOUT | Output | Signal output |
| VDD | Power | Positive supply |
| GND | Ground | Ground rail |

**LVS Setup**
- Configured as top-level subcircuit
- Enabled netlist export for layout tools

## Critical Issue

**Transistor channel lengths too small for Sky130 PDK**
- Minimum practical length: ~150 nm
- Must resize before layout to avoid DRC/LVS errors

## Next Steps

1. Increase transistor channel length
2. Generate netlist
3. Import to Magic VLSI
4. Layout and verify (DRC/LVS)

---

**Stack**: Xschem · Magic VLSI · Sky130 PDK