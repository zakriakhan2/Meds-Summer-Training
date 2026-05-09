# Computer Architecture - Lecture Notes

## Lecture 1: Introduction
This lecture covers CMOS basics.[cite: 1]

### Topics Covered
* NMOS and PMOS[cite: 1]
* CMOS inverter[cite: 1]

---

## Lecture 2: CMOS Constraints, Scaling, and Programmable Logic

### Topics Covered

#### 1. CMOS Behavior & The "AND" Gate Problem
* **Transistor Strengths:**
    * **NMOS:** Strong at passing '0' (Ground), weak at passing '1'.[cite: 1]
    * **PMOS:** Strong at passing '1' (Power), weak at passing '0'.[cite: 1]
* **The Inversion Necessity:** Because of these strengths, CMOS gates are naturally inverting.[cite: 1]
* **AND Gate Realization:** Unlike the **NAND** gate (4 transistors), an **AND** gate requires an extra inverter stage (6 transistors total), leading to increased area and latency.[cite: 1]

#### 2. Performance Metrics & Industry Trends
* **Moore’s Law:** The observation that transistor density doubles approximately every two years, driving the evolution of computing power.[cite: 1]
* **Power Consumption:** The relationship between switching frequency, voltage, and heat dissipation.[cite: 1]
* **Latency:** Understanding **Propagation Delay**—the time required for a signal to travel through gates and settle at the output.[cite: 1]

#### 3. Combinational Logic Foundations
* **Boolean Algebra:** Application of identities (De Morgan's, Distributive, etc.) to minimize logic expressions.[cite: 1]
* **Combinational Circuits:** Design of memoryless systems where the output depends solely on current inputs.[cite: 1]

#### 4. Programmable Logic Arrays (PLA)
* **Structure:** Implementation of logic using a programmable **AND-plane** followed by a programmable **OR-plane**.[cite: 1]
* **Full Adder Case Study:** Mapping the truth tables for **Sum** and **Carry-out** into a PLA architecture.[cite: 1]

---

## Repository Overview
This repo covers the design and simulation of key digital components, focusing on hardware efficiency and memory architecture.[cite: 1]

### Combinational Logic
* **Comparators:** Logic for magnitude comparison ($A > B$, $A < B$, $A = B$).[cite: 1]
* **ALU:** Core arithmetic and logic operations.[cite: 1]
* **Tri-State Buffers:** Managing high-impedance states for bus sharing and preventing signal contention.[cite: 1]

### Sequential & Memory Systems
* **SRAM Cell:** Analysis of the 6T (6-transistor) cell structure and data stability.[cite: 1]
* **Memory Arrays:** Building scalable storage using row decoders, word-lines, and bit-lines.[cite: 1]
* **Sense Amps:** Speeding up data reads by detecting small voltage swings.[cite: 1]

### Tech Stack
* **Languages:** Verilog / VHDL[cite: 1]
* **Tools:** ModelSim, Vivado, or similar HDL simulators[cite: 1]
* **Focus:** Gate-level optimization and timing verification[cite: 1]

---

## Advanced Projects
Projects focused on Finite State Machine (FSM) optimization and the internal architecture of FPGA hardware.[cite: 1]

### Finite State Machines (FSM)
* **Moore vs. Mealy:** Implementing both architectures comparing Moore (outputs based on state) and Mealy (outputs based on state and inputs).[cite: 1]
* **Encoding Schemes:**
    * **Binary Encoding:** Minimizing the number of flip-flops.[cite: 1]
    * **One-Hot Encoding:** Optimizing for speed and reducing combinational logic depth at the cost of more registers.[cite: 1]
    * **Output Encoding:** Mapping state bits directly to outputs for glitch-free performance.[cite: 1]

### FPGA Architecture
* **Configurable Logic Blocks (CLBs):** Understanding LUT-based logic implementation.[cite: 1]
* **Interconnects:** How programmable switch matrices route signals.[cite: 1]
* **Programming:** The bitstream flow from HDL code to hardware physical mapping.[cite: 1]

### Technical Focus
* FSM state reduction and timing closure.[cite: 1]
* Synthesis and implementation on FPGA fabric.[cite: 1]

---

## Timing & Analysis

### Delay Metrics
* **Propagation Delay ($t_{pd}$):** The maximum time from input change to the output reaching its final value.[cite: 1]
* **Contamination Delay ($t_{cd}$):** The minimum time an output remains stable after an input change.[cite: 1]

### Path Analysis
* **Critical Path:** The longest path in the design that limits the maximum operating frequency.[cite: 1]
* **Sequencing Overhead:** The combined time penalties from setup/hold times and propagation delays of flip-flops.[cite: 1]
* **Glitches:** Identification of temporary unwanted transitions caused by mismatched path delays in combinational logic.[cite: 1]

### Clock & Synchronization
* **Clock Skew:** Analysis of spatial variation in clock arrival times across different registers.[cite: 1]
* **Delay Modeling:** Understanding how gate and wire delays impact overall system performance.[cite: 1]

### Key Objectives
* Optimizing for timing closure and preventing race conditions.[cite: 1]
* Calculating maximum clock frequency based on path constraints.[cite: 1]

---

## Verilog Implementation

### Hierarchical Design
* **Modular Structure:** Organizing code into **Top**, **Sub**, and **Leaf** modules for scalability and readability.[cite: 1]
* **Module Instantiation:** Connecting components using named and positional port mapping.[cite: 1]

### Modeling Styles
* **Dataflow:** Using `assign` statements for combinational logic.[cite: 1]
* **Behavioral:** Implementing logic via `always` blocks (procedural assignments).[cite: 1]
* **Structural:** Explicitly calling gate primitives to define hardware topology.[cite: 1]

### Syntax & Implementation
* **Combinational vs. Sequential:**
    * **Comb:** Blocking assignments (`=`) and sensitivity lists using `*`.[cite: 1]
    * **Seq:** Non-blocking assignments (`<=`) triggered by clock edges (`posedge`/`negedge`).[cite: 1]
* **Verilog Fundamentals:** Syntax for wires, registers, bit-vectors, and parameters.[cite: 1]

### Focus
* Code modularity and hardware abstraction levels.[cite: 1]
