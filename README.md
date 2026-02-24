# 1st-Experiment-
Design Common Source Amplifier using NMOS MOSFET in (tsmc 018nm) technology in Laboratory using LT spice software.
# Introduction to Amplifier.
# what is Amplifier?
An amplifier is an electronic device.
It increases the strength of a weak signal.The output signal is stronger but has the same shape as input.
# what is Common source Amplifier?
A Common Source (CS) amplifier is a MOSFET amplifier in which the source terminal is common to both input and output, the input is applied at the gate, and the output is taken from the drain, providing voltage amplification with 180° phase shift.
# Circuit diagram of CS Amplifier?
https://github.com/lecsinchanamn/1st-Experiment-/blob/f6182b314198c72725b89d32e6bece3ce04d7454/CS%20Amplifier.jpg
# what is role of R_D in circuit?
1. Develops Output Voltage:
   - The output is taken across R_D.
   - Changes in drain current cause voltage changes across R_D → amplified output.

2. Controls Gain:
   - Voltage gain A_v ≈ -g_m * R_D
   - Higher R_D → Higher voltage gain

3. Limits Current:
   - Protects the MOSFET by limiting the drain current.
# What is role of VDD in Circuit?
1. Provides Bias:
   - Supplies DC voltage needed to properly **bias the MOSFET** in the active region.

2. Enables Amplification:
   - Allows the MOSFET to conduct drain current.
   - Without VDD, there will be **no output voltage**.

3. Determines Output Swing:
   - Maximum output voltage is limited by VDD.
   - Higher VDD → larger possible output swing (up to MOSFET limits).
# which are the Different types of analysis required for CS Amplifier?
# DC Analysis:
   ----------------
   - Purpose: To find the **operating point (Q-point)** of the MOSFET.
   - Determines:
     - Drain current (I_D)
     - Drain voltage (V_D)
     - Gate voltage (V_G)
     - Source voltage (V_S)
   - Ensures the MOSFET operates in the **active/linear region** for proper amplification.

 # AC (Small-Signal) Analysis:
   -------------------------------
   - Purpose: To study the **amplification characteristics** of the circuit.
   - Determines:
     - Voltage gain (A_v)
     - Input impedance (R_in)
     - Output impedance (R_out)
     - Phase relationship between input and output
   - Uses **small-signal model** of MOSFET. 
# Transient Analysis:
   -----------------------
   - Purpose: To study the **time-domain response** of the amplifier.
   - Determines:
     - Response to a **step input** or **pulse input**
     - **Rise time, fall time, and delay**
     - How output **follows input** over time
   - Important for **digital signals and switching applications**.

# Transfer Characteristic of CS Amplifier

1) Definition:
Transfer characteristic shows the relationship between
Input Voltage (Vin or VGS) and Output Voltage (Vout or VDS).

2) Condition 1: Cut-off Region
If VGS < Vth
→ MOSFET is OFF
→ ID = 0
→ Vout = VDD (maximum)
→ No amplification

3) Condition 2: Saturation Region (Active Region)
If VGS > Vth and VDS ≥ (VGS - Vth)
→ MOSFET is ON
→ ID flows
→ Vout decreases
→ Amplification happens
→ Output is inverted

4) Condition 3: Triode Region
If VDS < (VGS - Vth)
→ MOSFET fully ON
→ Vout becomes very small
→ No proper amplification

5) Important Point:
When Vin increases → Vout decreases
(Phase inversion of 180°)

# AIM
Design and Simulate the Common Source Amplifier NMOS MOSFET and Using (time 018nm) technology in Laboratory using LT spice software.
# specification table.
Supply Voltage (VDD)          = 2 V
Power Consumption (P)         = 1.2 mW
Drain Current (ID)            = 200 µA
Load Capacitance (CL)         = 0.7 pF
NMOS Channel Length (Ln)      = 480 nm
Technology                     = TSMC 0.18µm CMOS
# What are the Parameter need to find using this Specification?
1. Drain current (ID).
2. Drain Resistor (RD).
3. Channel Width of NMOS MOSFET (Wn).
# Theoretical calculation.
https://github.com/lecsinchanamn/1st-Experiment-/blob/4eb58277f3577c238c9830dbc94bbbaad6c93e22/Theoretical%20calculation.jpg
https://github.com/lecsinchanamn/1st-Experiment-/blob/539bd8e45ddfd2f8a521f9c4c4e8886142225d7e/Theoretical%20Calculationn.jpg
# DC Analysis (DC Sweep):
 what is it:
 Slowly change the input voltage and observe the output
 Why we do it:
 1. Find the operating point (Q-point) of the NMOS transistor
 2. Check if amplifier works in the correct region (not cut-off or saturation)

 How it works:
1. Sweep the gate voltage V_GS from low to high
 2. Measure drain current I_D or drain   voltage V_D
 3. Plot output vs input
For the simulation the values are:

DC OFFSET = O.9.
AMPLITUDE =10m.
FREQUENCY =1KHz.
AC AMPLITUDE =1.
# Circuit diagram 

# Tabular Table 
https://github.com/lecsinchanamn/1st-Experiment-/blob/92252573f8d650efbfd744b3ac2eeb6477148e4c/DC%20Sweep2.jpg
# Transint Analysis
# Input and Output both Transient Analysis.
The input voltage (Vin) is shown in blue, and the output voltage (Vout) is shown in green.The output voltage has a larger amplitude than the input, showing that the circuit amplifies the signal.
The output is inverted compared to the input; when the input increases, the output decreases.Phase inversion is typical for a common-source (CS) MOSFET amplifier.
https://github.com/lecsinchanamn/1st-Experiment-/blob/f5971c55f62360e626d7ad8ed8c6f8231ca7cb46/Transient%20Analysis1.jpg
# Only Output Transient Analysis.
This figure shows the transient output waveform of the common source amplifier. A sinusoidal input signal is applied to the gate, and the output voltage is observed at the drain. The output waveform is sinusoidal and centered around the bias voltage, which indicates that the MOSFET is operating in saturation region and the amplifier is working correctly.
https://github.com/lecsinchanamn/1st-Experiment-/blob/24f7d11d635a07b63a65ff90698175622721f181/Transient%20Analysis2.jpg
# Theoretical and Practical calculation 
https://github.com/lecsinchanamn/1st-Experiment-/blob/048edfa3a286f0dd83092382961f1c842364dea7/Theoretical%20%26%20practical%20TA.jpg
# DC Transfer characteristics.

1. Cut-off Region (MOSFET OFF)
Vin = LOW; Input voltage is very small
VGS < Vth; Gate-Source voltage below threshold
ID = 0; No drain current
Vout = VDD - ID * RD; Output voltage ~ VDD

2. Saturation Region (Amplifier ON)
Vin = MEDIUM; Input voltage moderate
VDS > VGS - Vth; Condition for saturation
ID = 0.5 * kn * (VGS - Vth) * (VGS - Vth); Drain current in saturation
Vout = VDD - ID * RD; Output voltage decreases with Vin
Small change in Vin → large change in Vout (amplification region)

3. Triode Region (MOSFET fully ON)
Vin = HIGH; Input voltage high
VDS < VGS - Vth; Condition for triode
ID = kn * ((VGS - Vth) * VDS - 0.5 * VDS * VDS); Drain current in triode
Vout = VDD - ID * RD; Output voltage ~ 0
# Circuit diagram and wave.
https://github.com/lecsinchanamn/1st-Experiment-/blob/5fa62d352d51f6517e0429daf9cd5fdd6998bd86/DC%20Analysis.jpg
# AC Analysis without Capacitor.
 
 # Calucation of Gain and Bandwidth 
Midband gain ≈ 2.8076 
nearly 3Gain in dB ≈ 8.48dB3 dB bandwidth ≈ 33.28
GHzGBP ≈ 11.4 × 33.28 GHz ≈ 379.392GHz (approx) 
The AC frequency response of the common-source MOSFET amplifier shows that the amplifier provides a stable and constant gain in the midband frequency range. 
This means the circuit amplifies the input signal properly without distortion at low and medium frequencies.
# Waveform.
https://github.com/lecsinchanamn/1st-Experiment-/blob/82837e6379d8681bc17520410a7338bb68fdfb51/AC%20analysis%20withoutC.jpg

# AC Analysis with Capacitor.

For AC analysis use (.ac dec 10 0.1 100G)
In AC analysis, capacitors affect the frequency response of the CS amplifier.
If a 10 pF capacitor is connected (usually as load capacitor. It affects the output
The frequency response was obtained to determine gain and bandwidth.

# Calculation of Gain and Bandwidth 
From AC plot (with CL = 10pF):
Midband gain ≈ 2.8076
nearly 3Gain in dB ≈ 8.48dB3 dB bandwidth ≈ 34.276 GHz
GBP ≈ 11.36 × 34.276 GHz ≈ 381.42GHz (approx) From the AC frequency response analysis of the MOSFET common-source amplifier.
# Circuit diagram and wave.
https://github.com/lecsinchanamn/1st-Experiment-/blob/6e1d1a7e0d14e1a95256a527c6614dc84da13289/AC%20analysis%20with%20C.jpg
# Result of experiment.
The all 4 Analysis of Common Source Amplifier like Analysis, DC Analysis, Transient Analysis, Transfer characteristics Analysis are Done under (tsmc018nm) using LT spice.

# Inferences.

 ✅ AC Analysis 
AC analysis is used when the input is alternating current (AC).
Voltage and current change with time (like sine wave).
We study how the circuit behaves at different frequencies.
It tells us gain, phase shift, and frequency response.
Example: CS amplifier signal analysis.

 ✅ DC Analysis 
DC analysisis used when the input is direct current (DC).
Voltage and current are constant (do not change with time).
We find biasing values like �.
It tells us whether MOSFET is in cutoff, triode, or saturation region.
Used to set the correct operating point (Q-point).

✅ Transient Analysis 
Transient analysis studies the circuit during switching or changing time.
It shows how voltage and current change from one condition to another.
Important for circuits with capacitors and inductors.
It gives the time response (charging and discharging).               Example: Capacitor charging curve.
