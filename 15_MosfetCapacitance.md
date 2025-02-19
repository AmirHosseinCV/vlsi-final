## Overview of Parameters

![image](https://github.com/user-attachments/assets/7490c4f9-5cac-494f-a6d6-36e3a77e6fc6)

![image](https://github.com/user-attachments/assets/af643c5b-be88-417d-88bb-4dc5248e7214)

**Junction Capacitance (Cj)**:

![image](https://github.com/user-attachments/assets/a858970e-512d-4c3e-9260-453caff84a3b)

![image](https://github.com/user-attachments/assets/4418236d-7be3-4865-8f47-b6a26eff60ae)

$\huge{technology = 2\lambda}$ => مثلا میگه تکنولوژی 0.18 => $2\lambda = 0.18$

## **1. Oxide Capacitance**

$$\Huge{C_{ox} = \frac{\epsilon_{ox}}{t_{ox}} = \frac{\epsilon_{0} \cdot \epsilon_{r}}{t_{ox}}}$$

* **Parameters:**
    *  $\Huge{C_{ox}}$: Capacitance per unit area of the gate oxide.
    *  $\Huge{\epsilon_{ox} = \epsilon_{0} \cdot \epsilon_{r}}$: Permittivity of the gate oxide material (typically silicon dioxide).
    *  $\Huge{\epsilon_{0} ~= 8.85 \times 10^{-12}}$
    *  $\Huge{\epsilon_{r}}$: Must be given, like $\Huge{\epsilon_{sio2} = 3.9}$
    *  $\Huge{t_{ox}}$: Thickness of the gate oxide layer.

## **2. Gate-Bulk Overlap Capacitance**

$$\Huge{C_{GSO} = C_{GDO} = C_{ox} \cdot x_d \cdot W = C_o \cdot W}$$

* **Parameters:**
    * $\Huge{C_{GSO}}$, $\Huge{C_{GDO}}$: Gate-source and gate-drain overlap capacitances, respectively.
    * $\Huge{x_d}$:  Length of the overlap region between the gate and source/drain.
    * $\Huge{W}$: Width of the transistor channel.
    * $\Huge{C_o}$:  Overlap capacitance per unit width.

## **3. Channel Capacitance**

* **Cut-off Region:**
   * $\Huge{C_{GCB} = C_{ox} \cdot W \cdot L}$  (Gate-to-body capacitance)
   * $\Huge{C_{GCS} = 0}$ (Gate-to-source capacitance)
   * $\Huge{C_{GCD} = 0}$ (Gate-to-drain capacitance)

## **4. Gate Capacitance**
* When transistor is **off**:
   * $\Huge{C_g = C_{gb} = \epsilon_{ox}WL/t_{ox} = C_{ox}WL}$ **( = $\Huge{C_{0}}$)**
* When transistor is **on**:
   * $\Huge{C_g = C_{gb} + C_{gs} + C_{gd}}$
* **Parameters:**
   * $\Huge{C_g}$: Total gate capacitance.
   * $\Huge{C_{gb}}$: Gate-to-body capacitance.
   * $\Huge{C_{gs}}$: Gate-to-source capacitance.
   * $\Huge{C_{gd}}$: Gate-to-drain capacitance.
   * $\Huge{\epsilon_{ox}}$: Permittivity of the gate oxide.
   * $\Huge{W}$: Width of the transistor.
   * $\Huge{L}$: Length of the transistor.
   * $\Huge{t_{ox}}$: Thickness of the gate oxide.
   * $\Huge{C_{ox}}$: Oxide capacitance per unit area.
   * $\Huge{C_0}$: Gate capacitance when the transistor is off (cutoff region).

* **Resistive Region:**
   * $\Huge{C_{GCB} = 0}$
   * $\Huge{C_{GCS} = \frac{1}{2} \cdot C_{ox} \cdot W \cdot L}$
   * $\Huge{C_{GCD} = \frac{1}{2} \cdot C_{ox} \cdot W \cdot L}$

* **Saturation Region:**
   * $\Huge{C_{GCB} = 0}$
   * $\Huge{C_{GCS} = \frac{2}{3} \cdot C_{ox} \cdot W \cdot L}$
   * $\Huge{C_{GCD} = 0}$

* **Parameters:**
    * $\Huge{C_{GCB}}$: Gate-to-body capacitance.
    * $\Huge{C_{GCS}}$: Gate-to-source capacitance.
    * $\Huge{C_{GCD}}$: Gate-to-drain capacitance.
    * $\Huge{L}$: Length of the transistor channel.

## **5. Junction Capacitance**

Diffusion = نفوذ

$$\Huge{C_{diff} = C_{bottom} + C_{sw} = C_j \cdot AREA + C_{jsw} \cdot PERIMETER}$$

$$\Huge{= C_j \cdot L_s \cdot W + C_{jsw} \cdot (2L_s + W)}$$

$$\Huge{C_{poly} = C_{poly (plate)} \cdot AREA + C_{poly (fringe)} \cdot PERIMETER}$$

$$\Huge{C_{total} = C_{diff} + C_{metal}}$$

![image](https://github.com/user-attachments/assets/af643c5b-be88-417d-88bb-4dc5248e7214)


* **Parameters:**
    * $\Huge{C_{diff}}$: Total diffusion capacitance (includes bottom and sidewall components).
    * $\Huge{C_{bottom}}$: Junction capacitance of the bottom-plate junction.
    * $\Huge{C_{jsw}}$: Junction capacitance of the side-wall junction.
    * $\Huge{C_j}$: Junction capacitance per unit area.
    * $\Huge{W}$: Width of the source/drain diffusion region.
    * $\Huge{L_s}$: Length of the source/drain diffusion region.

## Detailed Gate Capacitance

| Capacitance    | Cutoff            | Linear                | Saturation              |
| -------------- | ----------------- | --------------------- | ----------------------- |
| $\Huge{C_{gb}}$ (total) | $\Huge{C_0}$             | $\Huge{0}$                   | $\Huge{0}$                     |
| $\Huge{C_{gd}}$ (total) | $\Huge{C_{ox}Wx_d}$      | $\Huge{C_0/2 + C_{ox}Wx_d}$  | $\Huge{C_{ox}Wx_d}$            |
| $\Huge{C_{gs}}$ (total) | $\Huge{C_{ox}Wx_d}$      | $\Huge{C_0/2 + C_{ox}Wx_d}$  | $\Huge{2/3 C_0 + C_{ox}Wx_d}$ |

**Explanation of Parameters:**

*   **$\Huge{C_{gb}}$ (total):** Total gate-to-body capacitance.
*   **$\Huge{C_{gd}}$ (total):** Total gate-to-drain capacitance.
*   **$\Huge{C_{gs}}$ (total):** Total gate-to-source capacitance.
*   **$\Huge{C_0}$:**  Represents the gate capacitance when the transistor is in the cutoff region.
*   **$\Huge{C_{ox}}$:** Oxide capacitance per unit area. It depends on the thickness and dielectric constant of the gate oxide.
*   **$\Huge{W}$:** Width of the transistor.
*   **$\Huge{x_d}$:** Depletion region width.

**Regions of Operation:**

*   **Cutoff:** The transistor is off, and there is no channel formed between the source and drain.
*   **Linear:** The transistor is on, and a channel is formed. The current flowing through the channel is linearly proportional to the gate-to-source voltage.
*   **Saturation:** The transistor is on, but the channel is pinched off at the drain end. The current flowing through the channel is no longer linearly proportional to the gate-to-source voltage and reaches a saturation level.
