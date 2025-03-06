Differential amplifier

A differential amplifier is an electronic device used to compare two different electrical signals. 
It has two inputs and gives an output based on the difference between those two signals. 
The main job of this amplifier is to make the difference between the signals bigger so that it can be easily measured or used for other purposes.

Basic structure of differential amplifer :

![image alt](https://github.com/Nutan069/Linear-Integrated-Circuits-/blob/361596516fbf46458be4dda10c262b9e52651e7b/photo1.png)

A differential amplifier using MOSFETs compares two input signals, Vin1 and Vin2, and amplifies the difference between them. 
The circuit consists of two MOSFETs (M1 and M2), where the sources of both MOSFETs are connected to a common voltage, typically ground or a reference voltage.
The gates of MOSFET M1 and M2 are connected to the input signals Vin1 and Vin2, respectively. 
The drains of both MOSFETs are connected together, and typically a resistor is placed there to help obtain the amplified output.
A current source is also connected to the drains of both MOSFETs to provide a steady current.
The output voltage, which is the amplified difference between Vin1 and Vin2, is taken from the common drain of the MOSFETs.
This setup allows the differential amplifier to amplify the difference in the input signals, providing an output that is sensitive to their variations.

FOUR TYPES OF DIFFERENTIAL PAIR AMPLIFIER: 
Resistor-Loaded Differential Pair: 
*Uses resistors as the drain load.
*Simple design but has low gain due to large  requirements.
*Limited common-mode rejection and output swing.

Current Source-Loaded Differential Pair:
* Replaces Rss with Ideal current source.
* Improves gain.

Simple Current Source Differential Pair:
* Uses a single MOSFET as a current source.
* Gain increases still.

Active Load Differential Pair (MOSFET as Load):
* Both Iss and Rd are replaced with a mosfet .
* Gain is too high.

Design Question : 
![image alt](https://github.com/Nutan069/Linear-Integrated-Circuits-/blob/bdd7a83ef7bcfd3c24aa70c864a82b3c4429e721/photo2.png)

Circuit 1 : Resistor loaded differntial amplifier : 
![image alt](https://github.com/Nutan069/Linear-Integrated-Circuits-/blob/a5d4f5dec104c22e11851b9536e2b03309c2cfcb/photo3.png)

DC analysis :
![image alt](https://github.com/Nutan069/Linear-Integrated-Circuits-/blob/ba520b8d26dd3e376c8b5423908ca2015624340c/photo4.png)

Transient analysis :
![image alt](https://github.com/Nutan069/Linear-Integrated-Circuits-/blob/35ab6323c3df3df4b60088876c4baebcb9e5832e/photo5.png)
Gain = Vincm/voutcm = 50mV/200mV = 4 

Frequency response : 
![image alt](https://github.com/Nutan069/Linear-Integrated-Circuits-/blob/9007f69bc6b384c37129806dc22f8a0046531aa3/photo6.png)
Bandwidth = 178 GHz 

Circuit 2 : Current source Loaded differential amplifier :
![image alt](https://github.com/Nutan069/Linear-Integrated-Circuits-/blob/bb13f4db4f17466e41d5de7c36156b2299c00bc5/photo7.png)

DC analysis :
![image alt](https://github.com/Nutan069/Linear-Integrated-Circuits-/blob/5f3b1301fb99672e02ef5b57cde6931b787773a2/photo8.png)

Transient analysis :
![image alt](https://github.com/Nutan069/Linear-Integrated-Circuits-/blob/c6f449519d022bb881af6c691a7c057fdcdfa5c0/photo9.png)
Gain = Vincm/voutcm = 50mV/200mV = 4 

Frequency response : 
![image alt](https://github.com/Nutan069/Linear-Integrated-Circuits-/blob/6d9f0e2fabfc2b1d2891501b910599c6b0df6111/photo10.png)
Bandwidth = 178 GHz 

Circuit 3 : Simple current source (MOSFET as Current source) Differential amplifier :
![image alt](https://github.com/Nutan069/Linear-Integrated-Circuits-/blob/84cf7f6d07f48abce69d1ac4b0812d8344bde288/photo11.png)

Bias voltage calcultaion :
![image alt](https://github.com/Nutan069/Linear-Integrated-Circuits-/blob/5e033fc940d98a32a7be2f2f30c69f1485ad86ac/photo13.png)

DC analysis :
![image alt](https://github.com/Nutan069/Linear-Integrated-Circuits-/blob/219beaa1bc50c359c637a721cfe569e94ea45771/photo12.png)

Transient analysis :
![image alt](https://github.com/Nutan069/Linear-Integrated-Circuits-/blob/6e9eab07f02b76ab2945486d6393c9071c6b729f/Photo14.png)
Gain = Vincm/voutcm = 50mV/200mV = 4 

Frequency response :
![image alt](https://github.com/Nutan069/Linear-Integrated-Circuits-/blob/c411ca65a6c4053b1bd72d50fe92a6bc03eced23/photo15.png)
Bandwidth = 178 GHz 


Inference :
Larger Rss makes it harder for the transistors to amplify small signals, leading to reduced gain.
* Vincm must be within the range that keeps both input transistors ON and in saturation.Since Rss allows variations in current as it doesn't produce constant current we replace resistor with constant current source which provides stable output and gain.>
* Larger Amplitude Causes Early Distortion i.e at higher ampltitude transistor reaches saturation or cutoff earlier , limiting the range of valid Vincm.(example done for both 50mV and 100mV amplitude)
* Maximum input swing is the largest input voltage before distortion starts.
* When I replaced all things by mosfet , was not able to get the required output , later after managing W/L Vout was set . As there no parameters that Vout actually depends on we may not be able to vary Vout, so there was little difference in the gain. 
* When we set Ac phase as 180 for one of the input there was a high gain.
