# 2.-Design-implement-and-simulatioin-of-Integrator-and-Differentiator
**AIM:**
To design , implement and simulate  an integrator and differentiator circuits

**APPARATUS  and SOFTWARE REQUIRED:**
S.No	Name of the Apparatus	Range	Quantity
1.	Signal Generator	3 MHz	1
2.	DSO	30 MHz	1
3.	Dual RPS	(0 – 30) V	1
4.	Op-Amp	µA741	1
5.	Bread Board		1
6.	Resistors	1K,10K,100K,	2
7.	Capacitors	0.1µF,0.01µF	1
8.	Connecting wires and probes	As required	
9.  LT SPICE software

**THEORY:**

**INTEGRATOR**
A circuit in which the output voltage waveform is the integral of the input voltage waveform is the integrator. Such a circuit is obtained by using a basic inverting amplifier configuration if the feedback resistor Rf is replaced by a capacitor Cf . The expression for the output voltage is given as,
Vo = - (1/Rf C1 ) ∫ Vi dt

Here the negative sign indicates that the output voltage is 180 0 out of phase with the input signal. Normally between fa and fb the circuit acts as an integrator. Generally, the value of fa < fb . The input signal will be integrated properly if the Time period T of the signal is larger than or equal to Rf Cf . That is,
T ≥ Rf Cf

The integrator is most commonly used in analog computers and ADC and signal-wave shaping circuits.

**DESIGN:**
 
To obtain the output of an Integrator circuit with component values R1Cf = 0.1ms , Rf = 10 R1 and Cf = 0.01 µF and also if 1 V peak square wave at 1000Hz is applied as input.
We know the frequency at which the gain is 0 dB, fb = 1 / (2π R1 Cf) Therefore fb = 	 Since fb = 10 fa , and also the gain limiting frequency fa = 1 / (2π Rf Cf)
We get , R1 =	and hence Rf = 	

**DIFFEERENTIATOR:**

The differentiator circuit performs the mathematical operation of differentiation; that is, the output waveform is the derivative of the input waveform. The differentiator may be constructed from a basic inverting amplifier if an input resistor R1 is replaced by a capacitor C1 . The expression for the output voltage is given as,
Vo = - Rf C1 ( dVi /dt )

Here the negative sign indicates that the output voltage is 180 0 out of phase with the input signal. A resistor Rcomp = Rf is normally connected to the non-inverting input terminal of the op-amp to compensate for the input bias current. A workable differentiator can be designed by implementing the following steps:
1.	Select fa equal to the highest frequency of the input signal to be differentiated. Then, assuming a value of C1 < 1 µF, calculate the value of Rf.
2.	Choose fb = 20 fa and calculate the values of R1 and Cf so that R1C1 = Rf Cf.

The differentiator is most commonly used in wave shaping circuits to detect high frequency components in an input signal and also as a rate–of–change detector in FM modulators.
 
**DESIGN (DIFFERENTIATOR):**

Design an op-amp differentiator that will differentiate an input signal with fmax = 100HZ Select fa = fmax = 100 HZ = 1 / 2πRFC1
Let C1 = 0.1μF
Then RF = 1 / 2π(102)(10-7)
= 15.9KΩ
Now choose fb = 10fa = 1 / 2πR1C1 Therefore, R1 = 1 / 2π(103)(10-7)
= 1.59KΩ Since RFCF = R1C1
We get, CF = (1.59*103*10-7) / 15.9*103
= 0.01μF


**PROCEDURE:**
1.	Connections are given as per the circuit diagram
2. + Vcc and - Vcc supply is given to the power supply terminal of the Op-Amp IC.
3.	By adjusting the amplitude and frequency knobs of the function generator, appropriate input voltage is applied to the inverting input terminal of the Op- Amp.
4.	The output voltage is obtained in the CRO and the input and output voltage waveforms are plotted in a graph sheet.

 
**INTEGRATOR:**
  **CIRCUIT DIAGRAM**
<img width="1600" height="1122" alt="image" src="https://github.com/user-attachments/assets/7282abe6-51d4-4cf8-94ae-5f3f373efce5" />

  **MODEL GRAPH:**
<img width="1600" height="900" alt="image" src="https://github.com/user-attachments/assets/4ec33202-52d5-405f-84ec-4f0f698ab9fb" />

  **TABULATION:**
 <img width="1600" height="900" alt="image" src="https://github.com/user-attachments/assets/c02c7ddb-f6ac-44db-b513-0b8fdee6897e" />
  **GRAPH**
  <img width="1080" height="1549" alt="image" src="https://github.com/user-attachments/assets/cf1b85c9-c8dc-48ee-aab3-47d2a052a841" />

**DIFFERENTIATOR:**
  **CIRCUIT DIAGRAM**
<img width="1600" height="1135" alt="image" src="https://github.com/user-attachments/assets/4a6f9d23-eac0-4e1b-a386-d80d716a571c" />
  **MODEL GRAPH:**
<img width="1600" height="1001" alt="image" src="https://github.com/user-attachments/assets/1498bfb8-8712-406c-89cc-1de7e1f51d64" />

  **TABULATION:**
<img width="1600" height="766" alt="image" src="https://github.com/user-attachments/assets/244af350-7151-481b-99ae-f0dd36c52ebc" />
  **GRAPH**
  <img width="1148" height="1556" alt="image" src="https://github.com/user-attachments/assets/a7d86d4b-d60a-4508-89f5-205e67abcf70" />

**LT-SPICE Tool:PROCEDURE:**
•	Double click on LT-Spice icon.
•	New schematic window open.
•	Pick and paste the required component from the library and draw the circuit diagram .
•	Complete the connection.
•	Save the file by giving file name.
•	Click on the run option ->click advanced open ->select Ac analysis->enter the amplitude time delay stop time value.
•	Click on the run option ->simulation window opens->place the probe ->output graph is obtained.
 
  **LT SPICE**
  **CIRCUIT and Waveform**
  **INTEGRATOR**
  <img width="1747" height="837" alt="(ADAIC) Integrator sine wave" src="https://github.com/user-attachments/assets/1cb8dfde-0ac2-4c09-a423-818cdc12b1f1" />
  <img width="1812" height="875" alt="Screenshot 2026-08-05 152157" src="https://github.com/user-attachments/assets/ea14a9ff-b2be-4034-8011-e2e54c72a192" />

  **DIFFERENTIATOR**
  <img width="1750" height="855" alt="(ADAIC) Differentiator sine wave" src="https://github.com/user-attachments/assets/20411985-9bc9-4a24-8ffd-1f8bea7d8682" />
  <img width="1733" height="902" alt="(ADAIC) Differentiator sq wave" src="https://github.com/user-attachments/assets/ac52eecb-aac3-4746-86ff-14cd9872db9d" />

**RESULT:**
Thus the Integrator and Differentiator are designed and simulated performance was successfully tested using op-amp IC 741 and LT SPICE.
