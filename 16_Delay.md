* Transistor Size = $\Huge{\frac{w}{l}}$ = این چیزی که توی ترانزیستور مینویسه
* Resistance of transistor = $\Huge{\frac{l}{w}}$ = معکوس سایز
* Unit pMOS resistance: $\Huge{2R}$ - Capacitance: C
* Unit nMOS resistance: $\Huge{R}$ - Capacitance: C
* **Scaling pMOS & nMOS:** (K = size of the transistor)
![image](https://github.com/user-attachments/assets/e5b044aa-a403-4d23-94ab-263ae4e0d1fc)

---------------
$$\Huge{T_{PHL} = 0.69 R_n C_L}$$

$$\Huge{T_{PLH} = 0.69 R_p C_L}$$

-----------

Equlivant transistor size:

Parallel:

$$\Huge{(\frac{w}{l})_{eq} = \sum_k (\frac{w}{l})_k = \frac{w_1 + w_2}{l}}$$

Sequential:

$$\Huge{(\frac{w}{l})_{eq} = \frac{w}{l_1 + l_2} = \frac{1}{n} (\frac{w}{l})}$$

--------

Delay has two parts (t = gh + p):
- Parasitic Delay: Independant of load (lead of the next gate) (p)
- Effort Delay: Regarding to load (load of the next gate) (gh)
