# EEE 351 Lab – Introduction

## Objective
This lab introduces the practical aspect of the course **EEE 351 – Microelectronic Devices and Circuits**, focusing on digital circuit design using open-source IC design tools.

Students will learn how to design, simulate, layout, and verify basic digital circuits.

---

## Course Focus
The lab work covers digital circuits, following earlier studies in device physics.  
The main circuits to be designed include:

- CMOS Inverter  
- Pass Gates  
- Transmission Gates  
- Multiplexer  
- Oscillator  

---

## Tools and PDKs

### Design Environment
Open-source IC design tools will be used for:
- Schematic capture  
- Simulation  
- Layout  
- Post-layout simulation  

### Process Design Kits (PDKs)
- **Sky130 PDK (SkyWater)** – course standard  
- **GF180 PDK (GlobalFoundries)** – used for demonstration  

> Note: The only difference between Sky130 and GF180 is the process node.  
> The design workflow remains the same.

---

## Design Workflow
The lab follows this sequence:

1. Schematic design  
2. Circuit simulation  
   - DC analysis  
   - AC analysis  
   - Transient analysis  
3. Layout creation  
4. Layout verification  
5. Post-layout simulation  

This process ensures that the layout behaves as expected compared to the original schematic.

---

## Interface Overview
The schematic tool is used for:
- Drawing circuit schematics  
- Running simulations  
- Testing circuit behavior before layout  

Although examples may include analog circuits such as operational transconductance amplifiers, the focus of this lab is on **digital circuits**.

---

## Key Notes
- Simulations are used to validate designs before layout.
- Post-layout simulations confirm that the fabricated layout meets expectations.
- All analysis methods taught in class (DC, AC, transient) are applied in this tool.

---

## Next Step
The next lab session will begin with the design of a **CMOS inverter**.

---
