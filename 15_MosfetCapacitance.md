## **1. Oxide Capacitance**

* Formula: $C_{ox} = \frac{\epsilon_{ox}}{t_{ox}}$

* **Parameters:**
    *  $C_{ox}$: Capacitance per unit area of the gate oxide.
    *  $\epsilon_{ox}$: Permittivity of the gate oxide material (typically silicon dioxide).
    *  $t_{ox}$: Thickness of the gate oxide layer.

## **2. Gate-Bulk Overlap Capacitance**

* Formula: $C_{GSO} = C_{GDO} = C_{ox} \cdot x_d \cdot W = C_o \cdot W$

* **Parameters:**
    * $C_{GSO}$, $C_{GDO}$: Gate-source and gate-drain overlap capacitances, respectively.
    * $x_d$:  Length of the overlap region between the gate and source/drain.
    * $W$: Width of the transistor channel.
    * $C_o$:  Overlap capacitance per unit width.


## **3. Channel Capacitance**

* **Cut-off Region:**
   * $$C_{GCB} = C_{ox} \cdot W \cdot L$$  (Gate-to-body capacitance)
   * $$C_{GCS} = 0$$ (Gate-to-source capacitance)
   * $$C_{GCD} = 0$$ (Gate-to-drain capacitance)

## **4. Gate Capacitance**
* When transistor is **off**:
   * $C_g = C_{gb} = \epsilon_{ox}WL/t_{ox} = C_{ox}WL$
   * $C_0 = C_{ox}WL$
* When transistor is **on**:
   * $C_g = C_{gb} + C_{gs} + C_{gd}$


* **Resistive Region:**
   * $C_{GCB} = 0$
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

## **5. Junction Capacitance**

* **Formula:** $C_{diff} = C_{bottom} + C_{sw} = C_j \cdot AREA + C_{jsw} \cdot PERIMETER = C_j \cdot L_s \cdot W + C_{jsw} \cdot (2L_s + W)$

* **Parameters:**
    * $C_{diff}$: Total diffusion capacitance (includes bottom and sidewall components).
    * $C_{bottom}$: Junction capacitance of the bottom-plate junction.
    * $C_{jsw}$: Junction capacitance of the side-wall junction.
    * $C_j$: Junction capacitance per unit area.
    * $W$: Width of the source/drain diffusion region.
    * $L_s$: Length of the source/drain diffusion region.

## Detailed Gate Capacitance

| Capacitance    | Cutoff            | Linear                | Saturation              |
| -------------- | ----------------- | --------------------- | ----------------------- |
| $C_{gb}$ (total) | $C_0$             | $0$                   | $0$                     |
| $C_{gd}$ (total) | $C_{ox}Wx_d$      | $C_0/2 + C_{ox}Wx_d$  | $C_{ox}Wx_d$            |
| $C_{gs}$ (total) | $C_{ox}Wx_d$      | $C_0/2 + C_{ox}Wx_d$  | $2/3 C_0 + C_{ox}Wx_d$ |

**Explanation of Parameters:**

*   **$C_{gb}$ (total):** Total gate-to-body capacitance.
*   **$C_{gd}$ (total):** Total gate-to-drain capacitance.
*   **$C_{gs}$ (total):** Total gate-to-source capacitance.
*   **$C_0$:**  Represents the gate capacitance when the transistor is in the cutoff region.
*   **$C_{ox}$:** Oxide capacitance per unit area. It depends on the thickness and dielectric constant of the gate oxide.
*   **$W$:** Width of the transistor.
*   **$x_d$:** Depletion region width.

**Regions of Operation:**

*   **Cutoff:** The transistor is off, and there is no channel formed between the source and drain.
*   **Linear:** The transistor is on, and a channel is formed. The current flowing through the channel is linearly proportional to the gate-to-source voltage.
*   **Saturation:** The transistor is on, but the channel is pinched off at the drain end. The current flowing through the channel is no longer linearly proportional to the gate-to-source voltage and reaches a saturation level.
