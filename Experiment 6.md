Current mirror circuit

A current mirror circuit is used to copy one active device’s input current to the output of other active devices. 
This kind of circuit is also known as an ideal current amplifier including the inverting design that can overturn the direction of current flow.

![image alt](https://github.com/Nutan069/Linear-Integrated-Circuits-/blob/21274730b051df500c73c42a065c0cb19688f4d1/0.png)

A MOSFET current mirror is a circuit that replicates a reference current using MOSFETs . 
It typically consists of two matched MOSFETs, where one is the reference transistor (M1) and the other is the output transistor (M2).
The drain current of M1 sets the reference current, and M2 mirrors this current.
Both MOSFETs are connected in such a way that their gate-source voltages (V_GS) are equal.
This ensures that the current in M2 mirrors the current in M1, assuming they are matched and operate in the saturation region.
The basic current mirror uses a single MOSFET as the reference and another to copy the current. 
Improved designs, such as the cascode current mirror, offer better accuracy and higher output impedance.
The mirror’s accuracy depends on matching MOSFETs and proper biasing.

Design Question : 

