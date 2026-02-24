# 1st-Experiment-
Design Common Source Amplifier using NMOS MOSFET in (tsmc 018nm) technology in Laboratory using LT spice software.
# introduction to Amplifier.
# what is Amplifier?
An amplifier is an electronic device.
It increases the strength of a weak signal.The output signal is stronger but has the same shape as input.
# what is Common source Amplifier?
A Common Source (CS) amplifier is a MOSFET amplifier in which the source terminal is common to both input and output, the input is applied at the gate, and the output is taken from the drain, providing voltage amplification with 180° phase shift.
# Circuit diagram of CS Amplifier?
CS Amplifier.jpg
# what is RD? 
1.Develops Output Voltage:
The amplified output is taken across �.
When drain current changes, voltage across � changes → gives amplified output.
2.Controls Gain:
Voltage gain � (approx).
Higher � → higher voltage gain.
3.Limits Current:
Protects MOSFET by limiting drain current.
CS Amplifier - Drain Resistor (R_D)

Definition:
-------------
R_D is the drain resistor in a Common Source (CS) amplifier.

Roles of R_D:
-------------
1. Develops Output Voltage:
   - The output is taken across R_D.
   - Changes in drain current cause voltage changes across R_D → amplified output.

2. Controls Gain:
   - Voltage gain A_v ≈ -g_m * R_D
   - Higher R_D → Higher voltage gain

3. Limits Current:
   - Protects the MOSFET by limiting the drain current.

Memory Tip:
-------------
R_D acts as a "signal translator":
- Converts current variations in the MOSFET into voltage variations at the output.
