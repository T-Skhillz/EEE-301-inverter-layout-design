# EEE 301 Lab – Lab 1: Introduction to Digital IC Design

## Objective
This lab introduces the practical aspects of **EEE 301 – Microelectronics, Devices, and Circuits**, focusing on digital circuit design using open-source IC design tools.  

Students will learn how to design, simulate, layout, and verify basic digital circuits, which are the building blocks of complex digital systems.

---

## Importance of Basic Digital Circuits

Even simple circuits like:

- CMOS Inverter  
- Multiplexers  
- Pass Gates  
- Transmission Gates  
- Oscillators  

are **crucial components of modern processors and ICs**.  

For example, inside processors such as Apple’s M2, you will see these components repeatedly in:

- ALUs (Arithmetic Logic Units)  
- Control Units  
- Data paths  

Understanding these fundamentals is essential before moving to more complex digital IC systems.

### Relation to Processor Design (RISC-V Example)

RISC-V is an open-source Instruction Set Architecture (ISA), similar to:

- ARM (used by Apple)  
- x86 (used by Intel)  

Students can leverage RISC-V as a framework to design processors. Within processors, basic digital components like multiplexers and logic gates appear repeatedly, forming the building blocks of ALUs and control logic.

---

## Tools and PDKs

### Design Environment
Open-source IC design tools are used for:

- Schematic capture  
- Electrical simulation  
- Layout design  
- Post-layout verification  

### Process Design Kits (PDKs)
- **Sky130 PDK (SkyWater)** – standard for the course  
- **GF180 PDK (GlobalFoundries)** – used in demonstrations  

> Difference between Sky130 and GF180 is only the process node. Design workflow remains the same.

---

## IC Design Workflow

### 1. Idea / Concept
- Design starts as an idea or problem to solve.

### 2. Specifications
- Translate the idea into **clear, valid, and realizable specifications**.

### 3. Schematic Design
Schematic design includes:

- **Schematic Capture:** Draw the circuit diagram.  
- **Electrical Simulations:** Verify the circuit using:
  - DC Analysis  
  - AC Analysis  
  - Transient Analysis  
> Advanced analyses like noise or temperature are usually for analog ICs.

### 4. Layout Design (Physical Design)
- Create the physical representation of the circuit.
- Can be PCB or netlist-driven.

### 5. Design Rule Check (DRC)
- Ensure all layout rules are followed (spacing, layer alignment, etc.).  
- Rules vary by PDK and foundry.

### 6. Layout vs Schematic (LVS)
- Compare layout to original schematic to ensure the layout accurately represents the design.

### 7. Parasitic Extraction
- Identify unintended resistances and capacitances (parasitics).  
- Helps predict the real-world performance of the circuit.

### 8. Post-Layout Simulation
- Generate a netlist from the layout.  
- Run simulations (DC, AC, transient) to verify circuit performance matches schematic-level design.

### 9. Tape-Out (Optional / Advanced)
- Submit the verified design for fabrication.  
- Programs like Google-sponsored workshops enable real tape-out, but this is **optional** for the course.

---

## Summary Workflow Diagram

```text
Idea / Concept
      ↓
Specifications
      ↓
Schematic Design (Capture + Electrical Simulation)
      ↓
Layout Design (PCB / Netlist-driven)
      ↓
Design Rule Check (DRC)
      ↓
Layout vs Schematic (LVS)
      ↓
Parasitic Extraction
      ↓
Post-Layout Simulation
      ↓
Tape-Out (Advanced / Optional)
