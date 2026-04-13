**Overview**
A synthesizable, counter-based clock divider with a configurable divisor  parameter.
Designed as a clean RTL module suitable for FPGAs . The output clock toggles
every divisor input clock cycles, producing a 50% duty-cycle output.

**Output frequency formula:**



**Example: 50 MHz input with DIVISOR = 5 → 5 MHz output**

Port Description

| Port      | Direction  | Width | Description                      
|-----------|------------|-------|----------------------------------
| `clk`     | input      | 1-bit | Source clock signal              
| `rst`     | input      | 1-bit | Active-high synchronous reset    
| `clk_out` | output reg | 1-bit | Divided clock output             


# Frequency Divider in Verilog

## Overview

This project implements a **parameterized frequency divider** using Verilog HDL.
It generates a lower-frequency output clock from a high-frequency input clock using a counter-based approach.


## Features

* Configurable division factor using a parameter (`DIVISOR`)
* Synthesizable RTL design
* Simple and efficient counter-based implementation
* Verified using simulation and waveform analysis


## Working Principle

A counter increments on every clock cycle.
When the counter reaches the specified divisor value, the output clock toggles and the counter resets.

Output frequency is given by:

> f_out = f_in / (2 × DIVISOR)


## Simulation

* Simulator: Icarus Verilog (via EDA Playground)
* Waveform Viewer: EPWave

The design was tested using a Verilog testbench and verified through waveform observation.

## Results

* Input clock: High-frequency signal
* Output clock: Reduced frequency based on the divisor
* Correct division behavior confirmed via waveform

## Concepts Used

* Sequential Logic
* Counters
* Clock Division
* Flip-Flops
* Timing Analysis

## Future Improvements

* Programmable divider with runtime control
* Duty cycle correction
* FPGA implementation (Quartus)
* Multi-frequency output generation

How to use : 
-Open Intel Quartus Prime lite 
-New project
-Synthesize for Netlist and Run RTL simulation for Waveforms 
