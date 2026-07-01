# 40V DC Motor H-Bridge Controller

## Overview
This repository contains the design files, simulations, and documentation for a 40V DC motor H-Bridge circuit capable of bidirectional control. The design was developed using a multi-stage validation approach: verifying the high-voltage logic and bootstrap physics in **Proteus**, followed by physical footprint mapping and PCB routing in **KiCad**.

## Key Features
* **High-Voltage Operation:** Designed to safely switch a 40V motor supply rail.
* **Hardware Shoot-Through Protection:** Utilizes dual IR2104 half-bridge gate drivers with built-in dead-time insertion, preventing cross-conduction.
* **Bootstrap Circuitry:** Integrated 10µF capacitors and fast-recovery diodes to safely drive the high-side N-Channel MOSFETs.
* **Optimized Power Routing:** High-current paths (40V IN, Motor Outputs) are routed with 1.5mm traces, while logic signals use standard 0.25mm traces.
* **Thermal Management:** Features a continuous bottom-layer copper ground pour to dissipate heat and shield logic inputs from high-voltage switching noise.

## Core Components
* **Gate Drivers:** 2x IR2104 (DIP-8)
* **Power MOSFETs:** 4x IRF540N (N-Channel, TO-220)
* **Terminals:** 5.08mm screw terminal blocks (Power & Motor), 2.54mm pin headers (Logic)
* **Passives:** 20Ω series gate resistors, 10µF radial electrolytic capacitors

## Repository Structure
* `/KiCad/` - Contains the schematic (`.kicad_sch`), PCB layout (`.kicad_pcb`), and 3D renders.
* `/Simulation/` - Contains the Proteus project files used to validate the gate driver logic.
* `/Docs/` - Contains the Bill of Materials (BOM) and the comprehensive Phase 2 Design Report (PDF).

## Getting Started
To view or modify the physical board layout:
1. Clone this repository.
2. Open the project file in [KiCad](https://www.kicad.org/).
3. To view the physical board, open the PCB Editor and press `Alt+3` to launch the 3D Viewer.
