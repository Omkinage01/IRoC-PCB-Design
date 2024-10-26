# Rover Control and Power Distribution PCB

## Overview
This repository contains the PCB design that centralizes **both control and power distribution** for a rover. Designed on EasyEDA, this PCB supports critical power and data connections required by various rover subsystems and manages all controls through STM32 microcontrollers. It is a 2-layer PCB, measuring 340mm x 355mm, and fits seamlessly onto the rover chassis.

## Key Features
- **Processor and Control Integration**: Houses three STM32 "black pill" controllers for comprehensive control over all rover functions. Each STM32 is equipped with a Serial Wire Debug (SWD) interface, connected via XH2.54 connectors for straightforward code uploading and debugging.
- **Subsystem Management**: Data and power connections are strategically routed to subsystems based on chassis position—manipulators, wheel motors, and steering systems are each fully controlled through this PCB.
- **Safety**: Integrated kill switches, subsystem-specific switches, and seven glass fuses tailored to subsystem requirements provide robust safety and protection.
- **Connectivity**: XT-60 connectors for power connections, XH 2.54 connectors for data connections, and screw terminal blocks for secondary connections. Power Over Ethernet (POE) integration supports data communication powered directly from a 24V battery.
- **Troubleshooting Flexibility**: Double-routing for each STM32 allows repurposing of motor pins for alternative components, with data outputs routed to screw terminals for simplified debugging and expansion.

## Specifications
- **Dimensions**: 340mm x 355mm
- **Layers**: 2
- **Voltage Requirements**: 12V and 24V
- **Trace Width Calculations**: Calculated based on IPC-2221 standards for external layers

## Schematic & Design Files
- **PCB Design**: [OSHWA PCB Design Link](https://oshwlab.com/omkinage/temppcb)
- **Schematics**: Available in the `schematics` folder in this repository.

## Getting Started
1. Clone this repository.
2. Review the PCB layout in EasyEDA or compatible EDA software.
3. Follow the **User Guide** for setup and assembly instructions, ensuring all connections match specified voltage and current requirements.

## Components
- **STM32 Controllers**: Three STM32 "black pill" units for control of all rover subsystems.
- **Motor Drivers**: Four mounting holes for easy integration with motor drivers.
- **Power Connections**: XT-60 connectors for main power, and XH connectors for data.
- **POE and Ethernet Connectivity**: Direct 24V battery connection for communication and power.

## Design Calculations
- **Trace Width**: Based on IPC-2221 standards for external layers.
- **Parameters**: k = 0.048, b = 0.44, c = 0.725
- **Formulas**:
  - Area [mils²] = Current (Amps) * {k * (Temperature Rise [°C])^b}^(1/c)
  - Width [mils] = Area [mils²] / {Thickness [oz] * 1.378 [mils/oz]}

## Acknowledgments
Special thanks to MaRS Club for their support and resources.
