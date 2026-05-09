# Computer Architecture & Digital Logic Design - Complete Course Notes

This repository contains comprehensive lecture notes and design documentation covering CMOS basics, computer architecture, performance metrics, and FPGA implementation strategies.

---

## 1. CMOS Fundamentals & Logic Gates

### CMOS Basics
* **NMOS Transistor:** Strong at passing '0' (Ground), weak at passing '1' (VDD)[cite: 1].
* **PMOS Transistor:** Strong at passing '1' (VDD), weak at passing '0' (Ground)[cite: 1].
* **The Inversion Necessity:** Due to these inherent transistor strengths, CMOS gates are naturally inverting, such as NAND and NOR gates[cite: 1].

### The "AND" Gate Problem
Realizing an **AND** gate in CMOS is more complex than a **NAND** gate:
* **NAND Gate:** Requires only 4 transistors[cite: 1].
* **AND Gate:** Requires a NAND gate followed by an inverter, totaling 6 transistors[cite: 1].
* **Impact:** This results in increased silicon area and higher propagation latency compared to naturally inverting gates[cite: 1].

---

## 2. Performance Metrics & Scaling

### Industry Trends
* **Moore’s Law:** The observation that transistor density doubles approximately every two years, which drives the evolution of computing power[cite: 1].
* **Power Consumption:** Defined by the relationship between switching frequency, voltage, and heat dissipation[cite: 1].
* **Delay Metrics:**
    * **Propagation Delay ($t_{pd}$):** The maximum time from an input change until the output reaches its final value[cite: 1].
    * **Contamination Delay ($t_{cd}$):** The minimum time an output remains stable after an input change[cite: 1].

### Path Analysis & Timing
* **Critical Path:** The longest path in a design that limits the maximum operating frequency[cite: 1].
* **Glitches:** Temporary unwanted transitions caused by mismatched path delays in combinational logic[cite: 1].
* **Clock Skew:** Spatial variation in clock arrival times across different registers[cite: 1].

---

## 3. Combinational Logic Foundations

### Boolean Algebra & Optimization
* Application of identities like De Morgan's and Distributive laws to minimize logic expressions and reduce hardware[cite: 1].
* **Combinational Circuits:** Memoryless systems where the output depends solely on current inputs[cite: 1].

### Key Components
* **Comparators:** Logic for magnitude comparison such as $A > B$, $A < B$, and $A = B$[cite: 1].
* **ALU (Arithmetic Logic Unit):** Core component for arithmetic and logic operations[cite: 1].
* **Tri-State Buffers:** Manages high-impedance states for bus sharing to prevent signal contention[cite: 1].

### Programmable Logic Arrays (PLA)
* **Structure:** Implementation of logic using a programmable **AND-plane** followed by a programmable **OR-plane**[cite: 1].
* **Case Study:** Mapping truth tables for **Sum** and **Carry-out** in a Full Adder into a PLA architecture[cite: 1].

---

## 4. Sequential & Memory Systems

### Memory Architecture
* **SRAM Cell:** Analysis of the **6T (6-transistor)** cell structure and its data stability[cite: 1].
* **Memory Arrays:** Built using row decoders, word-lines, and bit-lines for scalable storage[cite: 1].
* **Sense Amps:** Circuits that speed up data reads by detecting small voltage swings[cite: 1].

### Finite State Machines (FSM)
* **Moore vs. Mealy:**
    * **Moore:** Outputs depend only on the current state[cite: 1].
    * **Mealy:** Outputs depend on both the current state and the current inputs[cite: 1].
* **Encoding Schemes:**
    * **Binary Encoding:** Minimizes the number of flip-flops used[cite: 1].
    * **One-Hot Encoding:** Optimizes for speed and reduces combinational logic depth at the cost of more registers[cite: 1].
    * **Output Encoding:** Maps state bits directly to outputs for glitch-free performance[cite: 1].

---

## 5. FPGA Architecture & Implementation

### Internal Hardware
* **Configurable Logic Blocks (CLBs):** Understanding logic implementation based on Look-Up Tables (LUTs)[cite: 1].
* **Interconnects:** Programmable switch matrices used to route signals[cite: 1].
* **Programming Flow:** The process of converting HDL code into a bitstream for physical hardware mapping[cite: 1].

### Design Objectives
* Optimizing for **timing closure** and preventing race conditions[cite: 1].
* Calculating maximum clock frequency based on path constraints[cite: 1].
* Synthesis and implementation on FPGA fabric[cite: 1].

---

## 6. Hardware Description Language (HDL) - Verilog/VHDL

### Hierarchical Design
* **Modular Structure:** Organizing code into **Top**, **Sub**, and **Leaf** modules for better scalability[cite: 1].
* **Module Instantiation:** Connecting components using named or positional port mapping[cite: 1].

### Modeling Styles
* **Dataflow:** Using `assign` statements for combinational logic[cite: 1].
* **Behavioral:** Implementing logic via `always` blocks for procedural assignments[cite: 1].
* **Structural:** Explicitly calling gate primitives to define hardware topology[cite: 1].

### Syntax & Implementation
* **Combinational Logic:** Uses blocking assignments (`=`) and sensitivity lists using `*`[cite: 1].
* **Sequential Logic:** Uses non-blocking assignments (`<=`) triggered by clock edges like `posedge` or `negedge`[cite: 1].
* **Verilog Fundamentals:** Syntax for wires, registers, bit-vectors, and parameters[cite: 1].

---

## Tech Stack
* **Languages:** Verilog / VHDL[cite: 1]
* **Tools:** ModelSim, Vivado, or similar HDL simulators[cite: 1]
* **Focus:** Gate-level optimization and timing verification[cite: 1]
