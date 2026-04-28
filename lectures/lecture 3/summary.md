
This repo covers the design and simulation of key digital components, focusing on hardware efficiency and memory architecture.

### Combinational Logic
* **Comparators:** Logic for magnitude comparison ($A > B$, $A < B$, $A = B$).
* **ALU:** Core arithmetic and logic operations.
* **Tri-State Buffers:** Managing high-impedance states for bus sharing and preventing signal contention.

### Sequential & Memory Systems
* **SRAM Cell:** Analysis of the 6T (6-transistor) cell structure and data stability.
* **Memory Arrays:** Building scalable storage using row decoders, word-lines, and bit-lines.
* **Sense Amps:** Speeding up data reads by detecting small voltage swings.

### Tech Stack
* **Languages:** Verilog / VHDL
* **Tools:** ModelSim, Vivado, or similar HDL simulators
* **Focus:** Gate-level optimization and timing verification
"""

file_path_v2 = "Digital_Logic_Summary_v2.md"
with open(file_path_v2, "w") as f:
    f.write(md_content_v2)
