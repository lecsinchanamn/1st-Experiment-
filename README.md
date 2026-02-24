# 1st-Experiment-
Design Common Source Amplifier using NMOS MOSFET in (tsmc 018nm) technology in Laboratory using LT spice software.
# Introduction to Amplifier.
# what is Amplifier?
An amplifier is an electronic device.
It increases the strength of a weak signal.The output signal is stronger but has the same shape as input.
# what is Common source Amplifier?
A Common Source (CS) amplifier is a MOSFET amplifier in which the source terminal is common to both input and output, the input is applied at the gate, and the output is taken from the drain, providing voltage amplification with 180° phase shift.
# Circuit diagram of CS Amplifier?
CS Amplifier.jpg
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

 
