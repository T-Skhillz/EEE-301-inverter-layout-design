# Adding a Load Capacitor for CMOS Inverter Simulation

## Overview

A capacitor is added to the inverter **only for simulation**. It models the real operating environment, where the inverter drives the inputs of other logic gates (e.g., NAND gates), which are inherently capacitive.

---

## Why the Capacitor is Needed

- Represents input capacitance of next stage
- MOSFET gates are capacitive
- Models transient response and delay
- Not intended for fabrication

---

## Selecting the Capacitor

1. Open component insertion menu
2. Use **schematic (SKM) library**
3. Search:

