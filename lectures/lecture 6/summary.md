
### Delay Metrics
* **Propagation Delay ($t_{pd}$):** The maximum time from input change to the output reaching its final value.
* **Contamination Delay ($t_{cd}$):** The minimum time an output remains stable after an input change.

### Path Analysis
* **Critical Path:** The longest path in the design that limits the maximum operating frequency.
* **Sequencing Overhead:** The combined time penalties from setup/hold times and propagation delays of flip-flops.
* **Glitches:** Identification of temporary unwanted transitions caused by mismatched path delays in combinational logic.

### Clock & Synchronization
* **Clock Skew:** Analysis of spatial variation in clock arrival times across different registers.
* **Delay Modeling:** Understanding how gate and wire delays impact overall system performance.

### Key Objectives
* Optimizing for timing closure and preventing race conditions.
* Calculating maximum clock frequency based on path constraints.
