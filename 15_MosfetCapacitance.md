**1. Oxide Capacitance**

* **Formula:**  $C_{ox} = \frac{\epsilon_{ox}}{t_{ox}}$

* **Parameters:**
    *  $C_{ox}$: Capacitance per unit area of the gate oxide.
    *  $\epsilon_{ox}$: Permittivity of the gate oxide material (typically silicon dioxide).
    *  $t_{ox}$: Thickness of the gate oxide layer.

**2. Gate-Bulk Overlap Capacitance**

* **Formula:** $C_{GSO} = C_{GDO} = C_{ox} \cdot x_d \cdot W = C_o \cdot W$

* **Parameters:**
    * $C_{GSO}$, $C_{GDO}$: Gate-source and gate-drain overlap capacitances, respectively.
    * $x_d$:  Length of the overlap region between the gate and source/drain.
    * $W$: Width of the transistor channel.
    * $C_o$:  Overlap capacitance per unit width.

**3. Channel Capacitance**

* **Cut-off Region:**
   * $C_{GCB} = C_{ox} \cdot W \cdot L$  (Gate-to-body capacitance)
   * $C_{GCS} = 0$ (Gate-to-source capacitance)
   * $C_{GCD} = 0$ (Gate-to-drain capacitance)

* **Resistive Region:**
   * $C_{GCB} = 0$ [cite: 11, 12, 13]
   * $C_{GCS} = \frac{1}{2} \cdot C_{ox} \cdot W \cdot L$
   * $C_{GCD} = \frac{1}{2} \cdot C_{ox} \cdot W \cdot L$

* **Saturation Region:**
   * $C_{GCB} = 0$
   * $C_{GCS} = \frac{2}{3} \cdot C_{ox} \cdot W \cdot L$
   * $C_{GCD} = 0$

* **Parameters:**
    * $C_{GCB}$: Gate-to-body capacitance.
    * $C_{GCS}$: Gate-to-source capacitance.
    * $C_{GCD}$: Gate-to-drain capacitance.
    * $L$: Length of the transistor channel.

**4. Junction Capacitance**

* **Formula:** $C_{diff} = C_{bottom} + C_{jsw} = C_j \cdot AREA + C_{jsw} \cdot PERIMETER = C_j \cdot L_s \cdot W + C_{jsw} \cdot (2L_s + W)$

* **Parameters:**
    * $C_{diff}$: Total diffusion capacitance (includes bottom and sidewall components).
    * $C_{bottom}$: Junction capacitance of the bottom-plate junction.
    * $C_{jsw}$: Junction capacitance of the side-wall junction.
    * $C_j$: Junction capacitance per unit area.
    * $W$: Width of the source/drain diffusion region.
    * $L_s$: Length of the source/drain diffusion region.

**Important Notes:**

* These formulas provide a simplified model of MOSFET capacitances. In reality, these capacitances are non-linear and vary with the applied voltage.
* The specific values of the parameters depend on the fabrication process and transistor dimensions.
* Understanding these capacitances is crucial for analyzing the dynamic behavior and speed of MOSFET circuits.
