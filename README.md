# EEE 301 – CMOS Inverter Layout Design

This repository contains the step-by-step work I did for my EEE 301 CMOS inverter design lab. It shows the full process from schematic design to simulation and finally layout using open-source VLSI tools.

Each folder represents one stage of the design flow, and each folder has its own README explaining what was done at that stage.

## Tools Used

* **Xschem** – for drawing the schematic
* **NGSpice** – for DC and transient simulations
* **Magic VLSI** – for layout design
* **Sky130 PDK** – technology library

## Project Stages

1. **Schematic Design**  
   Design of the CMOS inverter using NMOS and PMOS transistors.

2. **DC Analysis**  
   DC sweep simulation to observe the voltage transfer characteristics (VTC).

3. **Transient Analysis**  
   Time-domain simulation to check the switching behavior of the inverter.

4. **Layout Design**  
   Physical layout of the inverter following design rules.

Each stage is documented inside its own folder.

## How I Launched Magic with Sky130
```bash
export PDK_ROOT=/home/username/eda_tools/open_pdks/sky130
magic -rcfile /home/username/eda_tools/open_pdks/sky130/sky130A/libs.tech/magic/sky130A.magicrc
```

Xschem was used for schematic capture and NGSpice for simulations.

## Purpose of This Repository

* To understand how a CMOS inverter works
* To practice DC and transient analysis
* To learn how schematic design translates into physical layout
* To document my lab work clearly

## Repository Structure
```
EEE-301-inverter-layout-design/
│
├── schematic-design/
│   └── README.md
├── dc-analysis/
│   └── README.md
├── transient-analysis/
│   └── README.md
├── layout-design/
│   └── README.md
└── README.md
```

## Notes

This repository is mainly for learning and documentation purposes. It records my progress and understanding of CMOS inverter design using the Sky130 process.