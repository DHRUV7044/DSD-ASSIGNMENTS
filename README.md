# Digital System Design (DSD) Course Assignments

This repository contains Verilog RTL designs and testbenches implemented for the Digital System Design (DSD) laboratory course, simulated using open-source tools.

## Course Project Catalog

### Assignment 1: Full Adder Logic
- Implementations of a 1-bit full adder using three modeling styles: Dataflow (`fad.v`), Behavioral (`fab.v`), and Structural (`fas.v`).
- Testbenches (`fatbd.v`, `fatbb.v`, `fatbs.v`) with GTKWave timing diagrams (`fatbdwaveform.png` etc.).

### Assignment 2: Adder Architectures
- Comparative implementation of 4-bit/8-bit adder structures:
  - Carry Ripple Adder (`cra.v`)
  - Carry Lookahead Adder (`cla.v`)
  - Carry Bypass Adder (`cba.v`)
  - Carry Select Adder (`csa.v`)
- Testbenches and simulation wave traces (`clawave.png`, etc.).

### Assignment 3: Combinational Blocks
- Multiplexers: 2x1 (`m2x1.v`), 4x1 (`m4x1.v`), and generic $n$-to-1 (`mnx1.v`) implementations.
- Decoders: 2x4 (`d2x4.v`), 3x8 (`d3x8.v`).
- Demultiplexers: 1x2 (`dem1x2.v`), 1x4 (`dem1x4.v`), and $1$-to-$n$ channel demux (`dem1xn.v`).
- Encoders: Priority/special encoders and standard binary encoders.
- Custom logic gates designed solely using 2x1 multiplexers.

### Assignment 4: Advanced Arithmetic & Functions
- Multipliers: 8-bit & 16-bit Array Multipliers (`armu8.v`, `armu16.v`), and 8-bit & 32-bit Booth's Multipliers (`bomu8.v`, `bomu32.v`).
- Verilog Functions and Tasks implementation of Muxes, Demuxes, Encoders, and Decoders (`funcamdtask/`).

### Assignment 5: Modeling Comparisons
- Comparison between detailed structural (`struc_modl`) and high-level behavioral (`behv_modl`) design methodologies in Verilog.

### Assignment 6: Sequential Components & Finite State Machines (FSMs)
- **Barrel Shifters**: Left, right, and bidirectional universal shift registers.
- **Elevator Controller**: A multi-floor lift controller FSM (`d_lift.v`).
- **Register File**: A multi-port 16x16 register file configuration (`d_reg16x16.v`).
- **Sequence Detector**: FSM detecting the sequence "110" in both overlapping and non-overlapping modes.
- **Parity Generator**: Moore and Mealy FSM parity checkers (`d0_mofsm.v`, `d1_mefsm.v`).
- **Traffic Light Controller**: Traffic light sequence state machine (`d_tralgt.v`).

### Assignment 7: Memory Architectures
- LUT-based static RAM array models: 8-bit depth (`ram_8_bit/`) and 32-bit depth (`ram_32_bit/`) memory arrays.

## Simulation Setup
These designs were compiled and simulated locally using the open-source **Icarus Verilog** compiler (`iverilog`) and analyzed using the **GTKWave** waveform viewer:
1. Compile the Verilog files:
   ```bash
   iverilog -o sim_out structural_design.v testbench.v
   ```
2. Run simulation to produce the VCD dump file:
   ```bash
   vvp sim_out
   ```
3. View the waveforms:
   ```bash
   gtkwave wave_dump.vcd
   ```\n