# EEE 301 Lab – CMOS Inverter Design and Simulation

## Objective
Design and simulate a **CMOS inverter** using an open-source IC design tool.  
This session introduces:

- Device selection (NMOS, PMOS)  
- Capacitive load modeling  
- Schematic capture  
- Wiring and layout basics in the design interface  

---

## Reference
- Textbook: *Microelectronic Devices and Circuits* by Howen and Sodini  
- CMOS Inverter design: Figure 5.18C  
- Process Nodes:
  - SkyWater: 1.8V  
  - GlobalFoundries: 3.3V (used in demonstration)  

---

## CMOS Inverter Overview

- Consists of **NMOS** and **PMOS** devices.  
- A **capacitor** is included at the output to model the expected capacitive load.  
  - This simulates the environment where the inverter will drive other MOSFET gates.  
- Understanding capacitive loading is critical in digital circuits.

---

## Steps in Schematic Capture

1. **Start the IC design interface**
   - For demonstration: GlobalFoundries PDK  
   - For course: SkyWater PDK  

2. **Create a new schematic**
   - Click **Add → New Schematic**  

3. **Insert devices**
   - Click **Tools → Insert Symbol** (shortcut: `Shift + I`)  
   - Select the correct **library**:
     - SkyWater: `SkyWater PDK symbols`  
     - GlobalFoundries: `GF PDK symbols`  
   - Search for and select:
     - NMOS transistor  
     - PMOS transistor  

4. **Place devices on the schematic**
   - Drop devices into the workspace  
   - Rearrange for clarity:
     - Select device → Press `M` to move  

5. **Insert wiring**
   - Connect nodes using **Insert Wire** button or shortcut `W`  
   - Example connections for CMOS inverter:
     - Gates of NMOS and PMOS connected together (input)  
     - Drain of PMOS connected to drain of NMOS (output)  
     - Source of PMOS → VDD  
     - Source of NMOS → GND  

6. **Arrange power supply and output**
   - VDD at top  
   - GND at bottom  
   - Output node in the middle  

---

## Notes on the Interface

- Shortcuts differ from standard schematic tools; common ones:
  - `Shift + I` → Insert symbol  
  - `W` → Wire  
  - `M` → Move device  
- Always use the **PDK library devices**, not generic library devices.  
- Adjust workspace zoom for better placement and clarity.  

---

## Next Step

- Continue schematic capture until CMOS inverter is fully wired  
- Proceed to **electrical simulation** (DC, AC, transient) in the next session  

---
