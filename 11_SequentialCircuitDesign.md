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


## Static vs. Dynamic Memory

- **Static Memory**:
  - Preserves state as long as power is on.
  - Built using **positive feedback**.

- **Dynamic Memory**:
  - Stores state temporarily.
  - Based on **charge storage** in parasitic capacitors.

### Static Latches and Registers

- **Bistable Circuit**:
  - Static memories use **positive feedback** to create a bistable circuit with two stable states (0 and 1).

- **Cross-Coupled Inverter Pair**:
  - Provides a stable way to store a binary variable.

- **Additional Circuitry**:
  - Needed to control the memory states.
- **Types:**
  - SR Flip-Flops (it's SR Latches is the slides)
  - Multiplexer Based Latches
  - Resettable and enabled latches and flip-flops
  - Master-Slave Based Edge Triggered Register

![image](https://github.com/user-attachments/assets/2a94f4cd-d534-4192-8856-8fcfcc864982)


## SR Latches
- S = Set, R = Rest, once you set s=1 while clk is 1, Q becomes 1 and maintains its state.
- Consist of 6 nmos, 2 pmos. 
- No static paths between VDD and GND can exist **except during switching**.

![image](https://github.com/user-attachments/assets/3ff4292c-ff39-4e81-80d9-ee619c0b0c81)

## Multiplexer Based Latches
- Consist of 2 nmos, 2 pmos, 3 not.
- Inverters are working as buffers (strenthening the signal), too.
- NMOS transistors are good at passing a strong "0" (low voltage), and pmos transistors are the opposite. By combining an NMOS and a PMOS in parallel, you get the best of both worlds.
 
![image](https://github.com/user-attachments/assets/46fd3386-2c92-4f24-8c1f-1fd0d2ae0f12)

-------

Most practical sequencing elements require a **reset signal** to **enter a known initial state on
startup** and ensure **deterministic** behavior.

-------
