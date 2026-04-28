
### Hierarchical Design
* **Modular Structure:** Organizing code into **Top**, **Sub**, and **Leaf** modules for scalability and readability.
* **Module Instantiation:** Connecting components using named and positional port mapping.

### Modeling Styles
* **Dataflow:** Using `assign` statements for combinational logic.
* **Behavioral:** Implementing logic via `always` blocks (procedural assignments).
* **Structural:** Explicitly calling gate primitives to define hardware topology.

### Syntax & Implementation
* **Combinational vs. Sequential:**
    * **Comb:** Blocking assignments (`=`) and sensitivity lists using `*`.
    * **Seq:** Non-blocking assignments (`<=`) triggered by clock edges (`posedge`/`negedge`).
* **Verilog Fundamentals:** Syntax for wires, registers, bit-vectors, and parameters.

### Focus
* Code modularity and hardware abstraction levels.
