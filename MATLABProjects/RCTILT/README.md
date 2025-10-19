# Visual Analysis of Voltage and Tilt Percentage in RC High-Pass Circuits

## Project Description
This project presents a MATLAB-based simulation and visualization of the **charging behavior of an RC (Resistor-Capacitor) circuit**, focusing on how the voltage across the capacitor evolves over time when subjected to a constant input voltage. The core objective is to demonstrate the **transient response** and provide a **visual understanding** of how energy is stored within a capacitor in such circuits.

The simulation uses the **RC charging equation** to calculate the **output voltage (Vout)** and introduces a novel concept termed as the **"Tilt Percentage"**, representing the proportion of the input voltage that has been achieved by the capacitor at any given moment, expressed as a percentage. This provides an intuitive perspective on the progress of the charging process.

The MATLAB script models key electrical parameters, including resistance (R), capacitance (C), and time constant (τ), and generates **graphical outputs** in two subplots:
1. The first subplot shows the **exponential rise in output voltage** over time, representing the capacitor's charging process.
2. The second subplot displays the **Tilt Percentage**, offering an immediate visualization of how close the capacitor voltage is to the input voltage.

The simulation highlights that:
- The capacitor charges to approximately **63%** of the input voltage at **one time constant (τ)**.
- It achieves more than **99%** of the input voltage by **five time constants (5τ)**.
- The tilt percentage graph complements the voltage curve, providing an interpretable metric that links theoretical understanding with practical insight.

### Practical Relevance
This project aids students and engineers in understanding **first-order circuit dynamics** — particularly, how **RC circuits respond to time-varying signals**. It also serves as a fundamental educational tool for visualizing **transient behavior in analog circuits**, applicable in:
- Analog filter design  
- Signal processing circuit analysis  
- Transient modelling for control systems  

The simulation provides an **accessible, visual learning experience**, bridging theoretical circuit concepts with real-world analysis using MATLAB.
