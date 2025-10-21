Date - 21/10/25

Project Title: Design of a Closed-Loop P Controller (Simulink)

Objective:
To design and simulate a closed-loop Proportional (P) Controller in Simulink for a first-order plant and observe how the proportional gain (Kp) affects steady-state accuracy and response speed.

System Overview:
a) Plant transfer function:

G(s)=1/ (0.5s+5)

b) Controller:

C(s)=Kp

c) Feedback system transfer function:

T(s) = Kp/(0.5s + 5 + Kp) 	​

 	​
Simulation Details:
Input-Step input (amplitude = 1, step time = 0)
Controller-Gain block (Calculated Kp = 45 for ~90% accuracy)
Plant-Transfer Function block = 1 / (0.5s + 5)
Feedback-Unity feedback (H(s) = Gain = 1)
Output-Scope

Key Equations

Steady-State Output:
yss= kp /(5+kp)

Steady-State Error:
ess=1-yss

Time Constant:
tow=0.5 /(5+kp) 	​

Observations (Effect when Kp ↑):
Steady-state error-↓ decreases
Accuracy-↑ increases
Response speed-↑ increases (τ decreases)

Simulation Steps:

Open Simulink → Create a Blank Model.
Add these blocks:
Step Input
Gain (Kp = 45)
Transfer Function (1 / (0.5s + 5))
Sum (with signs: +, −)
Scope

3. Connect them as:
Step → (+) → Gain → Transfer Function → Output → feedback (−)

4. Set simulation time to 1 second.

5. Click Run.

Observe that the output reaches ~90% of input (steady-state ≈ 0.9).

Verification:
For Kp=45 (manually calculated for 90% accuracy- 10% error) :
yss=0.9
tow=0.01sec

System reaches:
~63% of final value at t = τ = 0.01s
~95% at t ≈ 3τ = 0.03s

Files in this Repository

p_controller.slx → Simulink model
p_controller_diagram.png → Block diagram
README.md → Project documentation

Future work / Extensions:
Implement PID (add I to remove steady‑state error and D to reduce overshoot).
Replace first‑order model with a 2‑state yaw model (ψ, r) and simulate disturbances.
Deploy on hardware: ESP32/STM32 running control loop, IMU for heading feedback, ESC for motor control, and record logs.