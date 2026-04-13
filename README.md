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


How to use : 
-Open Intel Quartus Prime lite 
-New project
-Synthesize for Netlist and Run RTL simulation for Waveforms 
