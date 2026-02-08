# 🔌 CMOS Inverter DC Analysis (ngspice)

![ngspice](https://img.shields.io/badge/Simulator-ngspice-blue)
![PDK](https://img.shields.io/badge/PDK-Sky130-green)
![Status](https://img.shields.io/badge/Status-Completed-success)

This project demonstrates the DC sweep (Voltage Transfer Characteristic) analysis of a CMOS inverter using **ngspice** and Sky130 device models. It investigates the inverter switching threshold and the impact of transistor sizing on noise margin and performance.

---

## 📌 Objectives

* Perform DC sweep analysis of a CMOS inverter
* Plot the Voltage Transfer Characteristic (VTC)
* Determine the switching threshold voltage (Vm)
* Study the effect of PMOS/NMOS sizing
* Prepare for physical layout design

---

## 🛠 Tools & Technologies

* **ngspice**
* **Sky130 PDK**
* **Xschem** (schematic capture)
* Linux environment

---

## ⚙️ DC Sweep Syntax

The DC sweep command follows this syntax:

```spice
.dc <source_name> <start_value> <stop_value> <step_value>
```

Example:

```spice
.dc Vin 0 1.8 0.01
```

This sweeps the input voltage from 0V to 1.8V in 0.01V steps.

---

## 🧪 Simulation Setup

1. Comment out transient analysis:

```spice
*.tran 1n 100n
```

2. Enable DC sweep:

```spice
.dc Vin 0 1.8 0.01
```

3. Run simulation and plot:
   * `V(out)`
   * `V(in)` (optional)

---

## 📊 Voltage Transfer Characteristic (VTC)

> 📷 *Insert plot image here*
> `plots/vtc.png`

The Voltage Transfer Characteristic (VTC) shows the relationship between the input and output voltages of the CMOS inverter.

Key observations:
* **Vin low → Vout high**
* **Vin high → Vout low**
* The point where `Vin ≈ Vout` is the **switching threshold (Vm)**

For this design:
```
Vm ≈ 1.6 – 1.7 V (for VDD = 3.3 V)
```

---

## 🔧 Effect of Transistor Sizing

### Case 1: PMOS width smaller than NMOS (Wp < Wn)

* Switching point shifts left
* Reduced noise margin for logic '0'
* Skewed VTC curve

❌ Not recommended

---

### Case 2: PMOS width larger than NMOS (Wp >> Wn)

* Switching point shifts right
* Reduced noise margin for logic '1'
* Narrow valid high-input range

❌ Not recommended

---

### ✅ Optimal Design (Balanced Inverter)

To achieve a symmetric transfer curve:

```
βₙ ≈ βₚ
```

Since electron mobility is higher than hole mobility:

```
Wₚ ≈ 2 × Wₙ
```

This results in:
* Switching point near **VDD/2**
* Maximum noise margins
* Reliable logic operation

---

## 📈 Engineering Significance

The switching threshold voltage directly affects:
* Noise margins
* Logic robustness
* Power consumption
* Propagation delay
* Reliability of digital systems

Proper transistor sizing is essential for functional silicon design.

---

## 🚀 Design Flow Progress

Completed:
* ✅ Schematic design
* ✅ DC sweep analysis

Next steps:
* 🔜 Physical layout (Magic / KLayout)
* 🔜 DRC (Design Rule Check)
* 🔜 LVS (Layout vs Schematic)
* 🔜 Parasitic extraction
* 🔜 Post-layout simulation

---

## 📂 Project Structure

```text
.
├── schematics/
│   └── inverter.sch
├── spice/
│   └── inverter_dc.spice
├── plots/
│   └── vtc.png
└── README.md
```

---

## 🧠 Key Takeaway

A properly sized CMOS inverter produces a symmetric voltage transfer characteristic with a switching threshold near half the supply voltage. Deviations in transistor sizing shift the switching point and degrade noise margins.

This project serves as the foundation for more complex CMOS digital circuit design and physical implementation.

---

## 📜 License

[Specify your license here, e.g., MIT, Apache 2.0, etc.]

## 👤 Author

[Your Name/GitHub Username]

---

**⭐ If you found this project helpful, please consider giving it a star!**