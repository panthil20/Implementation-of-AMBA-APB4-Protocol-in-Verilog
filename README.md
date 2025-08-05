# Implementation-of-AMBA-APB4-Protocol-in-Verilog

## Overview

The AMBA APB4 Protocol project implements the Advanced Peripheral Bus (APB) protocol, part of the AMBA (Advanced Microcontroller Bus Architecture) family. This protocol is designed to offer a low-complexity, low-power interface for communication with peripherals in modern processors. It is particularly suited for connecting low-speed peripherals such as timers, UARTs, GPIOs, and configuration registers, where high performance is not required.

## Protocol Architecture

**Main Idea:**
This project involves implementing the AMBA APB protocol, consisting of an APB master, an APB slave, and an external system (such as a CPU). The external system sends commands to the APB master, which then communicates these commands to the APB slave. Inside the APB slave, a cache memory is integrated to facilitate testing of write and read processes. The testbench simulates the external system, allowing for the verification of the protocol's functionality.

**Illustration:**
![APB_Arch]("C:\Users\PANTHIL\Downloads\APB4_Architecture.png")

### Key Architectural Features:

- **Non-Pipelined Bus Interface**: Ensures straightforward communication with peripherals, minimizing complexity.
- **Single Clock Edge Operation**: Simplifies timing and reduces power usage, critical for battery-operated devices.
- **Three-State Control**: The protocol operates in three distinct states—IDLE, SETUP, and ACCESS—to manage data transfer efficiently.
