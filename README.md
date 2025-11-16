# ESP32-Based Programmable Logic Controller (PLC)

This repository contains the complete hardware design, simulation resources, and supporting documentation for a custom PLC built using the ESP32-S3 MINI-1 module. The project focuses on implementing a compact controller with opto-isolated digital inputs, triac-based AC outputs, and a workflow that can be designed, simulated, and verified using KiCad and Proteus. The implementation emphasises predictable behaviour, clean hardware structuring, and reproducible functionality.

## Project Overview

The PLC design is centred on the ESP32-S3, offering sufficient GPIO and processing capability for basic control operations. The hardware provides independent optically isolated inputs, AC output channels with triac drivers, and a regulated 3.3 V supply through an LM2596-based converter. All field connections are exposed through screw terminals, and each channel includes an LED indicator for quick verification.

### Implemented Hardware Features

- Six opto-isolated digital inputs using PC817 devices, each with its own indicator LED.  
- Six AC output channels implemented using MOC3021 optotriac drivers and BTB16 triacs.  
- Regulated 3.3 V supply using an LM2596 buck converter with local decoupling.  
- Logical grouping of input and output terminals with physical separation between low-voltage and AC sections.  
- Indicator LEDs provided on every input and output channel for debugging and simulation.

## Hardware Design and Layout

All schematic and PCB development was completed using **KiCad**.  
The board uses a two-layer layout with clear routing discipline:

- ESP32 placed centrally for balanced GPIO routing.  
- Input and output terminals arranged on opposite sides.  
- Wide AC traces in the triac region with adequate clearances.  
- Mounting holes provided for enclosure or test setup integration.  
- 3D renders included for reference.

## Simulation and Functional Testing

The system was validated using **Proteus circut simulator**, using the same circuit implemented on the PCB.  
Simulation covered:

- Input optocoupler switching characteristics  
- Optotriac triggering at the outputs  
- LED indicators for I/O status  
- GPIO behaviour under simple test firmware  
- A basic ladder-logic routine for functional verification  


## Scope and Limitations

This design is intended for educational and experimental use.  
It does not include zero-cross detection and is not certified for industrial deployment or safety-critical applications.

## License

Open-source hardware under MIT license. You are free to modify, improve, or manufacture the board for personal or educational use.

## Credits

Certain circuit concepts follow standard opto-isolated input and triac-output practices commonly found in electronics references.  
All schematic work, PCB layout, and simulation implementation were independently created in KiCad and Proteus by **Shiva Projects** for educational use.



