BMS Project: Step 1 - Open-Loop Constant Current (CC) Baseline
This is the first step in building a Battery Management System (BMS) Charging Controller that ensures safe and efficient energy regulation.
Tools and Components used -
 1. Tools and Components Used
Modeling Environment- MATLAB / Simulink	
Battery Model- Simulink / Simscape Electrical
Power Source-	Controlled Current Source (CCS)	Represents the charger forcing a fixed current.
Visualization	Scope Block-	Displays the Voltage (V), Current (A), and State of Charge (SOC) over time.

 1. Goal and Verification
GOAL: To verify the baseline model of the Li-Ion battery's electrical response under simple open loop charging conditions.
OBJECTIVES:
a) Model Setup: Integrate the Li-Ion Battery model with the Constant Current Source.
b) Parameter Verification: Use a known battery (e.g., 7.2 V, 5.4 Ah) to confirm the model reacts to inputs.
c) Physics Validation: Prove that the model accurately captures the terminal voltage spike of the battery. 

2. Key Observations and Results
a) The current (A) remained flat and constant at 1 A, which confirms the model is operating in an open-loop (unregulated) state.
b) The battery's terminal voltage (V) jumped above the nominal 7.2 V and settled near 8.33 V.
c) SOC is Stable at 100% - confirmin that the initial state and battery capacity settings are correctly configured for the simulation.
