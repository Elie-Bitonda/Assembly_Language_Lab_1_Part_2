PIC16F877A LED Control and Traffic Light Simulation

This repository contains assembly language programs written for the PIC16F877A microcontroller. The goal of the project is to demonstrate basic digital output control using LEDs, as well as a simple traffic light sequence. All programs were developed using MPLAB and tested through simulation in Proteus.

The project includes two main examples. The first is a single LED blink program where an LED connected to RA0 turns ON and OFF repeatedly with a short delay of about 0.25 seconds. This example is meant to show how to configure a port as output and control a pin using basic assembly instructions.

The second example is a traffic light system implemented using three LEDs. The RED, YELLOW, and GREEN LEDs are connected to RA0, RA1, and RA2 respectively. The program turns each LED ON one at a time with an approximate one-second delay between transitions, then repeats the sequence continuously. This demonstrates simple sequencing and control of multiple outputs.

All related files for the project are included inside a ZIP folder. The ZIP contains the MPLAB assembly source files, the Proteus schematic files for both simulations, and images showing the expected simulation results in Proteus. This makes it easy to open the project, run the simulations, and verify the output without additional configuration.

The Proteus simulations use a PIC16F877A microcontroller with an external 4 MHz crystal oscillator and two 22 pF capacitors. LEDs are connected to PORTA pins through resistors and then to ground. A 5 V power supply is used in the simulation.

During execution, PORTA is first configured as an output port and cleared to ensure all LEDs start in the OFF state. The LEDs are then controlled using simple `BSF` and `BCF` instructions. Timing delays are created using nested software loops based on the 4 MHz clock frequency. The delays are approximate and intended for learning and demonstration purposes.

This project helps reinforce key embedded systems concepts such as port configuration, assembly language programming, software-based delays, and hardware–software integration using simulation tools. The design can be extended in the future by using hardware timers or interrupts for more accurate timing.

Author:  
Bitonda Tuyizere Elie  
Email: ebitonda@andrew.cmu.edu
