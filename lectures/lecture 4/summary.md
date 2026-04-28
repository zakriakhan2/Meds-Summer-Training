
Projects focused on Finite State Machine (FSM) optimization and the internal architecture of FPGA hardware.

### Finite State Machines (FSM)
* **Moore vs. Mealy:** Implementing both architectures comparing Moore (outputs based on state) and Mealy (outputs based on state and inputs).
* **Encoding Schemes:** * **Binary Encoding:** Minimizing the number of flip-flops.
    * **One-Hot Encoding:** Optimizing for speed and reducing combinational logic depth at the cost of more registers.
    * **Output Encoding:** Mapping state bits directly to outputs for glitch-free performance.

### FPGA Architecture
* **Configurable Logic Blocks (CLBs):** Understanding LUT-based logic implementation.
* **Interconnects:** How programmable switch matrices route signals.
* **Programming:** The bitstream flow from HDL code to hardware physical mapping.

### Technical Focus
* FSM state reduction and timing closure.
* Synthesis and implementation on FPGA fabric.
"""
