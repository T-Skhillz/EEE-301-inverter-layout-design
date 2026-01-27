# EEE 301 Lab – CMOS Inverter Design and Simulation

## Objective
Design and simulate a **CMOS inverter** using an open-source IC design tool.  
This session introduces:

- Device selection (NMOS, PMOS)  
- Capacitive load modeling  
- Schematic capture using Xschem  
- Wiring and layout basics  
- Simulation using NGSPICE  

---

## Reference
- Textbook: *Microelectronic Devices and Circuits* by Howen and Sodini  
- CMOS Inverter design: Figure 5.18C  
- Process Nodes:
  - SkyWater 130nm: 1.8V (course standard)  
  - GlobalFoundries 180nm: 3.3V (used for demonstration)  

---

## CMOS Inverter Overview

- Consists of **NMOS** and **PMOS** devices.  
- A **capacitor** is included at the output to model the expected capacitive load.  
  - Simulates the environment where the inverter drives other MOSFET gates.  
- Understanding capacitive loading is critical in digital circuits.

---

## Tools Needed

1. **Xschem**
   - Open-source schematic capture tool.  
   - Handles schematic design and integrates with SPICE simulation.  
   - Download: [https://xschem.sourceforge.io](https://xschem.sourceforge.io)

2. **NGSPICE**
   - SPICE-based circuit simulator used as the backend for simulations.  
   - Download: [http://ngspice.sourceforge.net/download.html](http://ngspice.sourceforge.net/download.html)

3. **SkyWater 130nm PDK**
   - Provides pre-defined devices: NMOS, PMOS, capacitors, resistors, and libraries.  
   - Download/clone: [https://github.com/google/skywater-pdk](https://github.com/google/skywater-pdk)

> Note: For demonstration, the instructor uses **GlobalFoundries 180nm PDK**, but the workflow is the same.

---

## Steps in Schematic Capture (Xschem)

1. **Start Xschem**
   - Load the PDK library (SkyWater or GF180)  
   - Set up directories for symbols and components  

2. **Create a new schematic**
   - Click **Add → New Schematic**  

3. **Insert devices**
   - Shortcut: `Shift + I` → Insert symbol  
   - Select devices from the PDK library:
     - NMOS transistor  
     - PMOS transistor  

4. **Place devices on the schematic**
   - Drop devices into the workspace  
   - Rearrange for clarity: select device → press `M` to move  

5. **Insert wiring**
   - Shortcut: `W` → insert wire  
   - CMOS inverter connections:
     - Gates of NMOS and PMOS → input  
     - Drains of NMOS and PMOS → output  
     - PMOS source → VDD  
     - NMOS source → GND  

6. **Arrange power supply and output**
   - VDD at top  
   - GND at bottom  
   - Output node in the middle  

---

## Notes on the Interface

- Xschem shortcuts differ from standard schematic tools:  
  - `Shift + I` → Insert symbol  
  - `W` → Wire  
  - `M` → Move devices  
- Always use **PDK devices**, not generic library devices  
- Adjust workspace zoom for clarity and better placement  

---

## Next Step

- Complete schematic capture for the CMOS inverter  
- Run **transient simulation** in NGSPICE to verify functionality  
- Proceed to layout or post-layout simulation as needed  

---
