# Computer Architecture - Lecture Notes

## Lecture 2: CMOS Constraints, Scaling, and Programmable Logic

### Topics Covered

#### 1. CMOS Behavior & The "AND" Gate Problem
* **Transistor Strengths:** * **NMOS:** Strong at passing '0' (Ground), weak at passing '1'.
    * **PMOS:** Strong at passing '1' (Power), weak at passing '0'.
* **The Inversion Necessity:** Because of these strengths, CMOS gates are naturally inverting.
* **AND Gate Realization:** Unlike the **NAND** gate (4 transistors), an **AND** gate requires an extra inverter stage (6 transistors total), leading to increased area and latency.

#### 2. Performance Metrics & Industry Trends
* **Moore’s Law:** The observation that transistor density doubles approximately every two years, driving the evolution of computing power.
* **Power Consumption:** The relationship between switching frequency, voltage, and heat dissipation.
* **Latency:** Understanding **Propagation Delay**—the time required for a signal to travel through gates and settle at the output.

#### 3. Combinational Logic Foundations
* **Boolean Algebra:** Application of identities (De Morgan's, Distributive, etc.) to minimize logic expressions.
* **Combinational Circuits:** Design of memoryless systems where the output depends solely on current inputs.

#### 4. Programmable Logic Arrays (PLA)
* **Structure:** Implementation of logic using a programmable **AND-plane** followed by a programmable **OR-plane**.
* **Full Adder Case Study:** Mapping the truth tables for **Sum** and **Carry-out** into a PLA architecture.

---

