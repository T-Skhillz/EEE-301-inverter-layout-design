# EEE 354 Lab – IC Design Flow: Schematic and Layout

## Objective
This session explains the IC design workflow in detail, covering schematic capture, electrical simulation, layout, design rule checks, and post-layout verification.

---

## Schematic Design

Schematic design consists of two main parts in open-source IC design tools:

1. **Schematic Capture**
   - Drawing the circuit diagram using the IC design tool.
   - Creating the representation of the circuit that will guide layout and simulation.

2. **Electrical Simulations**
   - Verify circuit behavior before physical layout.
   - Typical analyses:
     - **DC Analysis**  
     - **AC Analysis**  
     - **Transient Analysis**  
   - More advanced analyses (e.g., noise, temperature) are usually for analog IC design and are optional here.

> Schematic design ensures your circuit works in theory before moving to physical design.

---

## Physical Design (Layout)

After schematic design, the next step is **layout**, which is the physical representation of the circuit on silicon.  

### Key Steps:

1. **PCB / Netlist-driven Layout**
   - Layout is guided by the netlist generated from the schematic.
   
2. **Design Rule Check (DRC)**
   - Each foundry has its own design rules (PDK-specific).
   - Rules ensure physical spacing, layer alignment, and other constraints to avoid fabrication errors.
   
3. **Layout vs. Schematic (LVS)**
   - Compares your layout to the original schematic.
   - Ensures the physical design accurately reflects the intended circuit.

4. **Parasitic Extraction**
   - Identifies unintended capacitances and resistances introduced by layout.
   - Helps predict how parasitics may affect circuit behavior.

5. **Post-Layout Simulation**
   - Generate a netlist from the layout.
   - Simulate again (DC, AC, transient) to verify performance matches the original schematic.

6. **Tape-Out (Optional / Advanced)**
   - Submit the verified design for fabrication.
   - Usually requires participation in programs like **Google-sponsored workshops**.
   - For this course, focus is on steps 1–6. Step 7 (tape-out) is optional and advanced.

---

## Summary of Workflow

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
Tape-Out (Advanced)
