# ansys-convective-cooling-duct
# ME-645 Project: Convective Heat Transfer in a Cooled Duct

[cite_start]This repository contains the ANSYS Fluent setup files for a project completed for the **ME-645: Convective Heat Transfer** course at IIT Gandhinagar. The project investigates the thermal behavior of fluid flow (air and water) in a 3D rectangular duct that is cooled from its top surface.

[cite_start] 

## 🎯 Project Objectives

[cite_start]The primary goals of this simulation study were[cite: 17]:
* [cite_start]To plot the 2D temperature profile at the duct's exit (surface BCRQ) for two different geometries and inlet temperatures using **air** as the fluid[cite: 18, 19, 20].
* [cite_start]To conduct a parametric study to find the effect of **Height (H)**, **velocity (u)**, **top wall temperature (Ts)**, and **$\Delta T$ (Tamb,i - Ts)** on the final exit temperature[cite: 21].
* [cite_start]To compare the thermal behavior and exit temperature profiles when the fluid is switched from **air** to **water**[cite: 22].

## 💻 Simulation Methodology

The simulation was performed using **ANSYS Fluent**.

* [cite_start]**Solver:** Pressure-based, steady-state[cite: 58].
* [cite_start]**Physics:** The Energy equation and Laminar flow models were enabled[cite: 59].
* [cite_start]**Fluid:** The simulation was run for both **Air** [cite: 57] [cite_start]and **Water**[cite: 216], with constant properties.
* **Solution Methods:**
    * [cite_start]**Coupling:** SIMPLE scheme[cite: 61].
    * [cite_start]**Discretization:** Second Order for Pressure, Momentum, and Energy[cite: 61].
* [cite_start]**Meshing:** A tetrahedral mesh was used for both geometries[cite: 33, 49].

### Boundary Conditions
* [cite_start]**Inlet (ADSP):** Velocity inlet with a uniform velocity $u$ and temperature $T_{amb,i}$[cite: 14, 65, 82].
* [cite_start]**Top (PQRS):** Constant temperature wall at $T_s$[cite: 15, 67, 84].
* [cite_start]**Other Walls:** Insulated (zero heat flux)[cite: 15, 68, 85].

## 📊 Summary of Conclusions

[cite_start]The simulation results provided a clear understanding of the convective heat transfer within the duct[cite: 257].

### 1. Parametric Study Insights
* **Height (H):** Increasing the duct height $H$ resulted in a **higher** average exit temperature. [cite_start]This is because a larger fluid volume is further away from the cooling influence of the top wall[cite: 260].
* **Inlet Velocity (u):** Increasing the velocity $u$ resulted in a **higher** average exit temperature. [cite_start]This is due to the shorter residence time of the fluid in the duct, allowing less time for heat to be transferred to the cold wall[cite: 261].
* [cite_start]**Top Wall Temp (Ts):** Lowering the top wall temperature $T_s$ directly led to a **lower** average exit temperature, as expected[cite: 262].
* [cite_start]**$\Delta T$ (Tamb,i - Ts):** A greater $\Delta T$ (achieved by increasing the inlet temperature) increased the driving force for heat transfer, enhancing the overall cooling effect[cite: 263].

### 2. Air vs. Water Comparison
The choice of fluid had a major impact on the temperature profile:

* [cite_start]**Air:** Has a **high thermal diffusivity**[cite: 236]. [cite_start]This allows the cooling effect from the top wall to spread more widely and gradually through the fluid, creating a thick thermal boundary layer[cite: 73, 74, 264].
* [cite_start]**Water:** Has a **low thermal diffusivity** but high thermal conductivity and specific heat capacity[cite: 231, 237]. This results in a very **intense cooling effect** that is highly **localized in a thin layer** near the cold wall. [cite_start]The bulk of the fluid remains largely unaffected[cite: 265, 266].

## 🛠️ How to Use This Repository

This repository contains the ANSYS Fluent case and data files (`.cas.h5` / `.dat.h5`).

1.  Download the desired case file (e.g., `Case-1-Air.cas.h5`).
2.  Open ANSYS Fluent.
3.  Load the case file via `File > Read > Case...`.
4.  The complete setup (geometry, mesh, materials, boundary conditions, and solver settings) will be loaded.
5.  You can run the calculation or load the associated data file (`.dat.h5`) to proceed directly to post-processing and visualize the results.

## 👥 Project Group D

* [cite_start]Apratim Pandey (24250019) [cite: 3, 4]
* [cite_start]Mondeep Gohain (24250057) [cite: 5, 6]
* [cite_start]Rohit Radheshyam Jaiswar (24210082) [cite: 7, 8]
