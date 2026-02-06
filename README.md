# PIC16F877A LED Control & Traffic Light Simulation

This repository contains PIC16F877A assembly language programs demonstrating basic LED control and a traffic light system. The projects are developed using MPLAB and simulated in Proteus, focusing on embedded systems fundamentals such as I/O configuration, software delays, and microcontroller–hardware interfacing.

---

## Project Overview

The repository includes two main embedded system demonstrations:

### 1. Single LED Blink
A basic program that blinks one LED connected to RA0 with a short delay (~0.25 seconds). This example introduces digital output control using PIC assembly language.

### 2. Traffic Light System
A traffic light controller that sequentially activates RED, GREEN, and YELLOW LEDs connected to RA0, RA1, and RA2. Each LED remains ON for approximately one second before switching to the next.

---

## Included Files (Zipped Folder Contents)

All project-related files are organized and included inside a **ZIP folder** for easy access and reproduction of results. The ZIP folder contains:

- **MPLAB Assembly Source Files (.asm)**  
  - Single LED blink program  
  - Traffic light controller program  

- **Proteus Simulation Files**  
  - Complete circuit schematics for both projects  
  - PIC16F877A configuration with external crystal oscillator and LEDs  

- **Proteus Result Images**  
  - Screenshots showing the expected simulation results  
  - LED blinking behavior  
  - Traffic light sequence operation  

This structure allows the project to be easily opened, simulated, and verified without additional setup.

---

## Hardware Requirements (Proteus Simulation)

- PIC16F877A microcontroller  
- 4 MHz crystal oscillator  
- 2 × 22 pF capacitors  
- LEDs (Red, Yellow, Green, Blue)  
- Resistors (10 kΩ as used in the simulation)  
- 5 V power supply  
- Proteus Design Suite  

---

## Pin Connections

### Crystal Oscillator
- OSC1 (Pin 13) connected to the crystal
- OSC2 (Pin 14) connected to the crystal
- Each crystal pin connected to ground through a 22 pF capacitor

### LED Connections
| LED | PIC Pin | Description |
|----|--------|------------|
| Red | RA0 | Traffic light RED |
| Yellow | RA1 | Traffic light YELLOW |
| Green | RA2 | Traffic light GREEN |
| Blue | RA0 | Single LED blink |

Each LED is connected in series with a resistor and then to ground.

---

## Software Requirements

- MPLAB IDE / MPLAB X
- MPASM assembler
- Proteus (for simulation)

---

## Program Operation

### Initialization
- PORTA is configured as output
- All PORTA pins are cleared at startup

### Execution
- LEDs are controlled using `BSF` and `BCF` instructions
- Software delays are implemented using nested loops
- Timing is based on a 4 MHz system clock

---

## Delay Implementation

Delays are generated using software loops and general-purpose registers:

- Single LED blink: ~0.25 second delay
- Traffic light system: ~1 second delay per LED

These delays are approximate and intended for educational purposes.

---

## Proteus Simulation Results

### Single LED Blink
- LED connected to RA0 blinks ON and OFF continuously
- Confirms correct output configuration and timing logic

### Traffic Light System
- RED, GREEN, and YELLOW LEDs activate sequentially
- Demonstrates correct sequencing and multi-output control

---

## Learning Outcomes

This project demonstrates:
- PIC16F877A I/O port configuration
- Assembly language programming
- Software-based timing delays
- Embedded system simulation using Proteus
- Hardware–software integration

---

## Notes

- This project is intended for learning and demonstration purposes
- Software delays are not cycle-accurate
- The design can be extended using hardware timers or interrupts

---

## Author

Bitonda Tuyizere Elie 
Email: ebitonda@andrew.cmu.edu  

