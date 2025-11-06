# Sectional Design of a Turbojet Engine with FEA and CFD Analysis

[cite_start]**A self-initiated project to design, model, and validate the critical components of a turbojet engine, including a single-stage axial compressor, a high-pressure turbine, and a convergent-divergent nozzle.** [cite: 1, 6, 7, 10]

![[Add your best image here, like the final assembly render or the hand-drawn schematic]](https://placehold.co/800x400/333/fff?text=Your+Final+Project+Render)

---

## 1. Project Objectives

This project was broken down into three main phases:

* **1. [cite_start]Understanding:** To research and understand the complete working mechanism of an aerodynamic turbojet engine and the specific roles of the compressor, combustor, turbine, and nozzle[cite: 3, 4].
* **2. [cite_start]Component Design (Creo Parametric):** To perform the detailed 3D modeling of the primary rotating components, including a single-stage axial compressor and a high-pressure turbine stage[cite: 5, 6, 7].
* **3. [cite_start]Validation (Ansys & Creo):** To analyze the performance and integrity of the designs using engineering simulation tools[cite: 8].
    * [cite_start]**FEA:** Validate the turbine blade's structural integrity against centrifugal force[cite: 9].
    * [cite_start]**CFD:** Analyze the nozzle's thrust performance and compare it to a baseline design[cite: 10].

---

## 2. Component Design & Modeling (Creo Parametric)

All components were designed from foundational principles and modeled in Creo Parametric.

### 🔸 Single-Stage Axial Compressor
[cite_start]The compressor is designed to draw in and pressurize ambient air[cite: 37].

* [cite_start]**Airfoil:** A **NACA 65-series** airfoil profile was generated from a `.pts` coordinate file to ensure aerodynamic precision[cite: 63, 64].
* [cite_start]**Modeling:** The 3D blade was created using the **Blend tool**, applying both taper and twist from root to tip[cite: 65].
* [cite_start]**Assembly:** The final 25-blade rotor was created by patterning the single blade onto a revolved hub using the **Axis Pattern** feature[cite: 79].

### 🔸 High-Pressure Turbine
[cite_start]The turbine is designed to extract energy from the hot, high-pressure gas to drive the compressor[cite: 87, 88].

* [cite_start]**Airfoil:** After research, the **VKI LS-89** public domain airfoil was selected, as it is specifically designed for a high-pressure turbine stage and can handle high thermal loads[cite: 94].
* [cite_start]**Modeling:** The LS-89 coordinate data, which includes a blunt trailing edge for internal cooling, was imported and modeled using the **Blend tool** with a significant twist to maximize energy extraction[cite: 102, 103].
* [cite_start]**Assembly:** The 13-blade stage was patterned onto an intricate, webbed central disc designed to reduce weight while maintaining strength[cite: 107, 108].

### 🔸 Convergent-Divergent (C-D) Nozzle
[cite_start]An innovative C-D nozzle was chosen over a standard convergent design to maximize thrust[cite: 119].

* [cite_start]**Design:** This design is more efficient at high pressure ratios and allows the exhaust gas to be accelerated to **supersonic speeds**[cite: 120].
* [cite_start]**Modeling:** The nozzle's profile was sketched as a 2D half-profile and created as a 3D solid model in a single step using the **Revolve** feature[cite: 121, 122].

---

## 3. Analysis & Validation (Ansys & Creo)

The component designs were validated using FEA and CFD to prove their performance and structural integrity.

### 📊 FEA: Turbine Blade Structural Integrity

* [cite_start]**Objective:** To validate the turbine blade's structural integrity against the immense centrifugal forces at 15,000 RPM[cite: 130].
* [cite_start]**Software:** Creo [cite: 132]
* **Setup:**
    * [cite_start]**Material:** A custom material for **Inconel 718** was defined, with a yield strength of 1035 MPa[cite: 133].
    * [cite_start]**Loads:** The blade root was fully constrained, and a rotational load of **15,000 RPM** was applied[cite: 134].
* [cite_start]**Result:** The simulation showed a maximum von Mises stress of **440 MPa** at the blade root[cite: 175].
* [cite_start]**Conclusion:** With a maximum stress of 440 MPa against a yield strength of 1035 MPa, the design is validated with a **robust safety factor of 2.35**[cite: 175].

![[Add image of your FEA stress results]](https://placehold.co/600x300/333/fff?text=FEA+Stress+Analysis+on+Turbine+Blade)

### 🌊 CFD: Nozzle Thrust Performance

* [cite_start]**Objective:** To analyze and compare the thrust performance of the innovative C-D nozzle against a standard convergent nozzle[cite: 178].
* [cite_start]**Software:** Ansys Fluent [cite: 178]
* **Methodology:**
    1.  [cite_start]**Geometry:** The internal "fluid domain" of the nozzle was modeled in Creo[cite: 181].
    2.  [cite_start]**Meshing:** The fluid domain was imported into Ansys and discretized into a finite element mesh[cite: 184].
    3.  [cite_start]**Boundary Conditions:** Realistic physics were applied, including high-pressure/high-temperature at the inlet and ambient pressure at the outlet[cite: 187].
* [cite_start]**Result:** The simulation visualized the gas accelerating to supersonic speeds[cite: 195].
* [cite_start]**Conclusion:** The final thrust calculation confirmed that the **C-D nozzle produced an 8.1% thrust gain** over the standard convergent design under these optimized conditions[cite: 198].

![[Add image of your CFD velocity/pressure contours]](https://placehold.co/600x300/333/fff?text=CFD+Nozzle+Performance+Analysis)

---

## 4. Final Core Assembly

[cite_start]The final assembly represents the core rotational and exhaust section of the turbojet, often called the "spool"[cite: 125]. [cite_start]It integrates the 25-blade compressor and 13-blade turbine on a central shaft, followed by the C-D nozzle, demonstrating the complete aerodynamic flow path[cite: 125, 126, 127].

![[Add image of your final CAD assembly]](https://placehold.co/600x300/333/fff?text=Final+CAD+Assembly)

## 5. Project Deliverables

This repository contains all the primary deliverables for this project.

* **/1 - 3D CAD Models (Creo)/**:
    * `Compressor_Assembly.asm`
    * `Turbine_Assembly.asm`
    * `Nozzle.prt`
    * `Full_Spool_Assembly.asm`
* **/2 - Analysis & Simulation Files (Ansys/Creo)/**:
    * `Turbine_Blade_FEA.sim`
    * `Nozzle_CFD_Fluent.wbpj`
* **/3 - Design & Research Files/**:
    * `NACA_65_series.pts`
    * `VKI_LS_89.dat`
    * `Project_Report.pdf` (The source PDF)
