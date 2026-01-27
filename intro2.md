# EEE 354 Lab – Importance of Digital Building Blocks & IC Design Flow

## Objective
This session explains the importance of basic digital circuits (such as CMOS inverters and multiplexers) in complex integrated systems and introduces the IC design flow in a more intentional and structured way.

---

## Importance of Basic Digital Circuits

Although components like the CMOS inverter, multiplexer, pass gate, transmission gate, and oscillator may seem simple, they are extremely important. These basic blocks form the foundation of complex digital systems.

Inside modern processors (for example, Apple’s M2 processor), the internal structure is made up of many logic gates and basic digital components.

These small building blocks are what combine to form:
- Logic units  
- Arithmetic Logic Units (ALUs)  
- Control units  
- Complete processors  

This shows the importance of understanding and mastering these fundamental circuits.

---

## Relation to Processor Design (RISC-V Example)

RISC-V is an open-source Instruction Set Architecture (ISA), similar to:
- ARM (used by Apple)
- x86 (used by Intel)

Students interested in processor design can use RISC-V as a framework to build their own processors.

When examining processor internals such as:
- ALUs  
- Control units  
- Data paths  

we observe that multiplexers, inverters, and logic gates appear repeatedly. These elements are essential in building subtractors, adders, and decision logic.

Therefore, the digital part of this course focuses on designing these fundamental circuits because they are the core of all complex digital IC systems.

---

## Why This Lab Focuses on Digital Design

This course emphasizes:
- CMOS inverter design  
- Multiplexers  
- Pass gates  
- Transmission gates  
- Oscillators  

These are the **foundations of digital IC design** and must be well understood before moving to more advanced systems.

---

## IC Design Flow Overview

The IC design process follows a structured flow:

1. **Idea / Concept**
   - A design begins as an idea or problem to solve.

2. **Specifications**
   - The idea is translated into clear and realistic specifications.
   - Not all specifications are realizable; they must be practical and valid.

3. **Schematic Design**
   - The circuit is drawn using schematic capture tools.
   - Electrical simulations are performed at this stage.
   - This stage is also called schematic-level design.

4. **Simulation**
   - Electrical behavior is verified through:
     - DC analysis  
     - AC analysis  
     - Transient analysis  

This schematic and simulation stage is what will be carried out using the design interface in the lab.

---

## Key Notes
- Basic digital circuits are the building blocks of complex processors and ICs.
- RISC-V provides an open-source path for students interested in processor design.
- Design must start from valid and realizable specifications.
- Schematic capture and simulation are essential before layout design.

---

## Next Step
The next session will begin the practical design of a **CMOS inverter**.

---
