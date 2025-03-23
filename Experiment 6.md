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
![image alt](https://github.com/Nutan069/Linear-Integrated-Circuits-/blob/2fb70c52e1a9607f48c5be4de04dd79e1f851d62/a.png)
A)
For 1:1 mirror ratio
Iref = P/(2*V) 
     = 0.276 mA
![image alt](https://github.com/Nutan069/Linear-Integrated-Circuits-/blob/b91a853b60e568e4be84a6e53ca068f435b5fa1b/b.png)
For transistor M1 : L=180nm , W=3um;
For transistor M2 : L=180nm , W=3um;
For transistor M3 : L=180nm , W=3.6um;
![image alt](https://github.com/Nutan069/Linear-Integrated-Circuits-/blob/2c373491549ff4e8683c9a931c80975c050e037e/d.png)

For transistor M1 : L=500nm , W=8.33um;
For transistor M2 : L=500nm , W=8.33um;
For transistor M3 : L=500nm , W=10um;
![image alt](https://github.com/Nutan069/Linear-Integrated-Circuits-/blob/06f61f9e8aec2e71f85e921b41e7445c4e45cdaf/e.png)

For transistor M1 : L=1um , W=16.66um;
For transistor M2 : L=1um , W=16.66um;
For transistor M3 : L=1um , W=20um;
![image alt](https://github.com/Nutan069/Linear-Integrated-Circuits-/blob/50f06aabc820cd9f9eba95460c60668313443871/c.png)

As the channel length increases the current mirroring will take place more accuratly because channel length modulation decreases.

Transient analysis :
![image alt](https://github.com/Nutan069/Linear-Integrated-Circuits-/blob/259dcb7132d32697501e7932f89bd832b17aa91a/f.png)
Gain = vout/vin = -140mV/10mV = -14 V/V
Maximimum output swing = 1.17-0.26
                       = 0.91V

AC analysis :
![image alt](https://github.com/Nutan069/Linear-Integrated-Circuits-/blob/f5c2ba64355a16ae0ec50e23cf2ca57fbcfba5a6/g.png)
Bandwidth = 2.259 GHz

For mirror ratio 1:2 
Iref = P/(3*V) 
     = 0.185 mA
DC analysis :
For transistor M1 : L=180nm , W=3um;
For transistor M2 : L=180nm , W=6um;
For transistor M3 : L=180nm , W=4.75um;
![image alt](https://github.com/Nutan069/Linear-Integrated-Circuits-/blob/ba3356cbd4bdae14eacca825839d3a76c457d1d8/h.png)

Transient analysis :
![image alt](https://github.com/Nutan069/Linear-Integrated-Circuits-/blob/97a8e4057826381e18cf7012b40ba7fdae6191b3/i.png)
Gain = vout/vin = -140mV/10mV = -14 V/V

AC analysis :
![image alt](https://github.com/Nutan069/Linear-Integrated-Circuits-/blob/aaccd123f08338215906e68fceb8c86d9e4dc2ca/j.png)
Bandwidth = 1.367 GHz

B)Design the differential amplifier using the same design . perform DC anlysis, transient analysis and AC analysis .
![image alt](https://github.com/Nutan069/Linear-Integrated-Circuits-/blob/d545870cfdb5b6c7bbe530a7ff7cd3571e085868/k.png)

DC analysis:
![image alt](https://github.com/Nutan069/Linear-Integrated-Circuits-/blob/5defd48871ece35b01b53c3c775c34d8d2c47c36/l.png)

Transient analysis:
![image alt]()
Gain = vout/vin = -3.89 V/V

AC analysis :
![image alt]()
Bandwidth = 

Inference:
Current Duplication: The primary function of a current mirror is to duplicate a reference current, allowing it to be used in different parts of the circuit, providing consistent current sources for various components.
Transistor Matching: Accurate current mirroring depends on closely matched transistors. Differences in characteristics like threshold voltage or current gain can lead to discrepancies in the mirrored current
Impact of Output Impedance: The output impedance plays a crucial role in determining the precision of the mirrored current. Higher output impedance typically leads to better current regulation, making the circuit more reliable
