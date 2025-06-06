

# Monostable multivibrator using 555 timer IC .
## Aim
### Generate pulse of width 0.5 ms using input triggers.
## Theory
A monostable multivibrator, also known as a one-shot multivibrator, possesses a single stable state. It is designed to produce a single output pulse of a predetermined width (either high or low) when an external trigger pulse is applied.   

The operation begins when a trigger pulse initiates a timing cycle. This causes the output to change its state from the stable state. The duration for which the output remains in this temporary, unstable state is determined by the time constant of a resistor (R) and a capacitor (C) in its feedback network. Once this time constant elapses, the output automatically returns to its original stable state, where it will remain until another trigger pulse is received.   

Monostable multivibrators are capable of generating rectangular waveforms with significantly longer durations. The leading edge of the output waveform directly coincides with the application of the external trigger pulse. Conversely, the trailing edge of the output pulse is dictated by the RC time constant of the feedback components. By adjusting this RC time constant, it's possible to create a series of pulses, each having a fixed time delay relative to its corresponding trigger pulse.   

## Working
In a monostable multivibrator built with a 555 timer, the output remains in its stable state until a trigger is received. This stable state occurs when both the internal transistor and capacitor are essentially "shorted."

When the voltage at pin 2 of the 555 IC drops below a certain threshold, the output switches to a high state. This high state is referred to as the quasi-stable state. The circuit then transitions from its stable state to this quasi-stable state. At this point, the internal discharge transistor turns off, allowing the capacitor to begin charging towards the Vcc (supply voltage) through resistor R1. The charging time is governed by the time constant R1C1.   

As the capacitor charges, its voltage steadily increases. Once the capacitor's voltage exceeds 2/3 of Vcc, it triggers the internal control flip-flop, which in turn switches off the 555 timer IC. This action causes the output to return to its original stable (low) state from the quasi-stable state.   

The duration of this output pulse, often denoted as T, is calculated by the formula:
T=1.1×R×C

where R is in Ohms (Ω) and C is in Farads.   

Ultimately, in a 555 timer monostable multivibrator, the output typically stays low until a trigger input is applied. Upon triggering, the output goes high for a specific duration determined by the RC components, and then returns to its low state. This behavior is commonly used in "push-to-operate" systems where a single input press generates a controlled output pulse.   


Sources and related content
## Circuit Diagram:
![image](https://github.com/Nutan069/Linear-Integrated-Circuits-/blob/6c5bfbf6a11a8653c39031c3d1cc63ed64370d73/Screenshot%202025-05-27%20054614.png)

## Calculation:
Given that T=0.5ms and assume c=.1uF.

T=1.1RC



R =  0.5mS/(1.1×1uF) = 4.5454 KΩ.
 
## Output Waveform
![image](https://github.com/user-attachments/assets/4ff3113f-d845-4684-b053-e50b7d29faac)

In the above circuit when the trigger pulse is lesser then 1/3 Vcc, We get output as high.

## Inference
-The circuit's output defaults to a LOW state and remains there until an external trigger signal is applied.

•Once triggered, the output transitions to a HIGH state. It holds this high state for a specific duration, which is precisely controlled by the RC time constant of the circuit.

•In a practical example, by selecting a capacitor with a value of 0.1 µF, a resistor value of approximately 4.5454 KΩ was calculated to generate a pulse width of 0.5 ms.

•This experiment effectively illustrates how a 555 timer configured in monostable mode can be utilized to produce accurate and predetermined time delays.

# Astable multivibrator and monostable multivibrator using 555 timer IC
## Aim
## Generate pulse of width 0.5ms using 555 timer IC.
## Theory
An astable multivibrator, often called a "free-running" multivibrator, is a circuit that generates a continuous rectangular waveform. Unlike its monostable counterpart, it doesn't need an external trigger to switch its output state. Instead, the duration of its high and low output states is determined by two resistors and a capacitor connected externally to the 555 timer chip.   


In a differentiator amplifier circuit, the positions of the capacitor and resistor are swapped compared to an integrator. Here, the capacitor 
 is connected to the input of the inverting amplifier, while the feedback element across the operational amplifier remains a resistor 
 This circuit performs the mathematical operation of differentiation. Essentially, the faster or larger the change in the input voltage signal, the greater the input current, and consequently, the more pronounced the output voltage change will be, often appearing as a "spike." Similar to the integrator, the RC network formed by the resistor and capacitor plays a crucial role, with the capacitor's reactance 
 being particularly significant in the differentiator's performance.   

A clipper circuit is used to remove or "clip" specific portions of a waveform, such as negative voltage spikes. The output of this clipper circuit then serves as the trigger signal for a monostable multivibrator.   

A monostable multivibrator, also known as a one-shot, has only one stable state. Its purpose is to generate a single output pulse of a specific width (either high or low) when an external trigger pulse is applied. This trigger pulse initiates a timing cycle, causing the output to change its state. The output then remains in this second, unstable state for a duration determined by the RC time constant of its capacitor (C) and resistor (R), after which it automatically reverts to its original stable state. It will stay in this stable state until another input signal is received. Monostable multivibrators are capable of producing much longer rectangular waveforms. The rising edge of the output waveform coincides with the external trigger pulse, while the falling (trailing) edge is governed by the RC time constant of the feedback components. This RC time constant can be adjusted over time to produce a series of pulses, each with a fixed time delay relative to the original triggered pulse.
## Procedure
1.	Build the circuit as per the Circuit diagram.
2.	Calculate the resistor R and capacitor C for Astable multivibrator Differentiator, clipper and Monostable multivibrator.
3.	Analyze the capacitor charging and discharging Voltage per time.
4.	Analyze the ton period when input is triggered.


## Calculation
![WhatsApp Image 2025-05-25 at 10 27 49 PM](https://github.com/Nutan069/Linear-Integrated-Circuits-/blob/77e86e115af27084215585b2fcaa7870abb81cec/Screenshot%202025-05-27%20061805.png)

![WhatsApp Image 2025-05-25 at 10 27 50 PM](https://github.com/Nutan069/Linear-Integrated-Circuits-/blob/ba33664053e1d8ef66db316f7049b136712c273c/Screenshot%202025-05-27%20061805.png)


## Circuit Diagram:
![image](https://github.com/user-attachments/assets/b07bcbbe-72dd-4548-a828-e1ff5dc9cebd)


## Waveform
### Case 1:
![image](https://github.com/user-attachments/assets/bdcbd7d8-b042-44d8-a02f-16989a367a90)

First wave is output of Astable Multivibrator, Second waveform is Output of Differentiator Circuit output, 3rd wave is the output of Negative Clipper circuit and fourth waveform is output of Monostable Multivibrator pulse width is 0.5ms.

### Case 2:
![image](https://github.com/user-attachments/assets/bb0dabe9-f63f-4be1-9e6b-fbbc78f23174)

First wave is output of Astable Multivibrator, Second waveform is Output of Differentiator Circuit output, 3rd wave is the output of Negative Clipper circuit and fourth waveform is output of Monostable Multivibrator pulse width is 0.5ms.
 cap value .1u

 ### Case 3:

 in case 3 the ton<toff which is not possible in astable Multivibrator , thus we can use an inverter to invert the pulse generated.
 
![image](https://github.com/user-attachments/assets/62330045-4a0a-422d-b977-9699a629bb00)


 ![image](https://github.com/user-attachments/assets/5974cd20-b140-48e9-b307-9e661e8e4906)



First wave is output of inverted Astable Multivibrator, Second waveform is Output of Differentiator Circuit output, 3rd wave is the output of Negative Clipper circuit and fourth waveform is output of Monostable Multivibrator pulse width is 0.5ms.

## Inference
- Controlling ON and OFF Times Isn't Always Straightforward
We saw that changing resistor and capacitor values lets us control how long the signal stays ON and OFF. But it’s not always possible to get any values we want with the basic 555 timer setup.

- The 555 Timer Has Its Limits
In some cases (like when OFF time needs to be longer than ON), the normal 555 astable circuit can’t give us the result directly. That’s why in Case 3, we had to flip the signal using an inverter.

- Inverters Can Help Us Get the Waveform We Want
By adding a simple NOT gate (built using a transistor), we were able to reverse the timing — this gave us more flexibility in generating the waveform we needed.

- Very Short Pulses Need Precise Components
In Case 2, we worked with very fast pulses (just fractions of a millisecond). To do that, we needed low resistor and capacitor values — which also showed us the importance of accuracy and how component selection affects timing.

- We Can Detect Edges Using a Differentiator
A differentiator circuit helped us catch the exact moment the signal goes from LOW to HIGH. This is useful when we only want to react to changes, not the full pulse.

- Monostable 555 Gives Clean, Consistent Pulses
Finally, when we triggered a monostable 555 with those edges, we got clean, uniform pulses every time. This is super helpful when we need a reliable output regardless of input width.

| **Case** | **Configuration** | **What We Learned** |
|----------|-------------------|----------------------|
| **Case 1**<br>(ON = 0.2 ms, OFF = 0.3 ms) | Direct astable 555 output | Basic control of ON/OFF time using R1, R2, and C values works well within certain timing ranges. |
| **Case 2**<br>(ON = 0.1 ms, OFF = 0.05 ms) | High-speed pulse using small R and C | Fast switching is possible but requires precise low-value components. Useful for short pulse generation. |
| **Case 3**<br>(ON = 0.3 ms, OFF = 0.4 ms)<br>with inverter | Inverter used after 555 output | Shows how logical inversion helps overcome 555 timer’s limitations, allowing ON < OFF timing. |


# Simulation in Virtual Lab Astable Multivibrator
## Procedure:
1.	Connect the components as mentioned below: L1-L12, L14-L12, L16-L12, L4-L9, L8-L9, L10-L19, L3-L17, L11-L13, L7-L19, L6-L13, L2-L13, L5-L15, L18-L9.(For eg. click on 1 and then drag to 12 and so on.)
2.	Click on 'Check Connection' button to check the connections.
3.	If connected wrong, click on the wrong connection. Else click on 'Delete all connection' button to erase all the connections.
4.	Intially set R a=3.3 kΩ, R b=6.8kΩ, C=0.1µf, Vcc=5 V.
5.	Click on "Calculate" button.
6.	Now note the output voltage.
7.	Click on "Plot" button to plot Output Voltage, Capacitance Voltage
8.	Click on "Clear" button to clear the data.
9.	Repeat the experiment for another set of resistance value.
10.	Set the Resistance (Ra) value (1 kΩ - 10 kΩ).
11.	Set the Resistance (Rb) value (1 kΩ - 10 kΩ).
12.	Set the Capacitance (C) value (0.1 µf - 10 µf) .
13.	Set supply voltage (Vcc).

## Circuit Diagram
![image](https://github.com/user-attachments/assets/303eba91-66eb-4a6a-9dbc-12f03dbb176c)


## Otuput Waveform
Voltage Across the Capacitor: 
![image](https://github.com/user-attachments/assets/3894310a-e307-4e17-a570-e0371812d10f)


Output Waveform: -
![image](https://github.com/user-attachments/assets/df261aa6-19a1-41bf-82f9-d65b0f5742c9)



