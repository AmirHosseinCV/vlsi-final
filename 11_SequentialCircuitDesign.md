- **Latch**:
  - Transparent when the clock (`clk`) is high.
  - Opaque when the clock (`clk`) is low.

- **Flip-Flop**:
  - An edge-triggered device.
  - Copies `D` to `Q` on the **rising edge** of the clock (`clk`).
  - Ignores `D` at all other times.
 

## Timing Metrics for Sequential Circuits

### Key Timing Parameters
1. **Set-up Time ($t_{su}$)**:
   - Time that the data inputs must be valid **before clock transition**.
2. **Hold Time ($t_{hold}$)**:
   - Time the data input must remain valid **after the clock edge**.
3. **Worst-Case Propagation Delay ($t_{cq}$)**:
   - Time for the $D$ input to be copied to the $Q$ output.

---

### Additional Timing Considerations
- **Worst-Case Timing Constraint**:
  - Clock period ($T$) must satisfy:
    $$T \geq t_{su} + t_{pd} + t_{cq}$$
    Where $t_{pd}$ is the propagation delay of the logic.

- **Minimum Delay (Contamination Delay)**:
  - Denoted as $t_{cd}$ (minimum propagation delay or contamination delay).
  - Must satisfy:
    $$t_{cd\_{register}} + t_{cd\_{logic}} \geq t_{hold}$$

![image](https://github.com/user-attachments/assets/b9c2e177-30f5-40df-aad8-c4f06db9c5fe)


### Review of Timing Notations:

- **$t_{su}$ (Set-up Time)**:
  - The time duration that the data input must be valid **before the clock edge**.

- **$t_{hold}$ (Hold Time)**:
  - The time duration that the data input must remain valid **after the clock edge**.

- **$t_{cq}$ (Clock-to-Q Delay)**:
  - The time taken for the data at the input ($D$) to propagate to the output ($Q$) after the clock edge.

- **$t_{pd}$ (Propagation Delay)**:
  - The delay caused by logic elements between registers.

- **$t_{cd}$ (Contamination Delay)**:
  - The **minimum propagation delay** (also called contamination delay) of a signal through logic or registers.

### Summary of Key Relationships:
1. **Clock Period ($T$)**:
   $$T \geq t_{su} + t_{pd} + t_{cq}$$

2. **Hold Time Condition**:
   $$t_{cd\_{register}} + t_{cd\_{logic}} \geq t_{hold}$$

