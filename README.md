# MATLAB-Based Modelling and Performance Analysis of an Automatic Voltage Regulator (AVR)

## Project Overview

This project models and simulates an Automatic Voltage Regulator (AVR) using MATLAB and Control System Toolbox. The system is designed to study the voltage regulation performance of a synchronous generator using a closed-loop feedback control system.

The model consists of four main components: amplifier, exciter, generator, and voltage sensor. The project analyses the system's step response, stability, steady-state error, and transient performance under different amplifier gain values.

## Objectives

* Develop a mathematical model of an AVR using transfer functions.
* Simulate the closed-loop AVR system in MATLAB.
* Analyse the system's stability using pole locations.
* Calculate rise time, settling time, overshoot, and steady-state error.
* Compare AVR performance for different amplifier gains.
* Visualise system responses using MATLAB plots.

## System Components

| Component      | Gain | Time Constant |
| -------------- | ---: | ------------: |
| Amplifier      |   10 |         0.1 s |
| Exciter        |    1 |         0.4 s |
| Generator      |    1 |         1.0 s |
| Voltage Sensor |    1 |        0.01 s |

## Mathematical Model

The transfer functions of the amplifier, exciter, generator, and sensor are represented as:

$$
G_A(s)=\frac{K_a}{T_as+1}
$$

$$
G_E(s)=\frac{K_e}{T_es+1}
$$

$$
G_G(s)=\frac{K_g}{T_gs+1}
$$

$$
H(s)=\frac{K_s}{T_ss+1}
$$

The closed-loop AVR transfer function is:

$$
T(s)=\frac{G_A(s)G_E(s)G_G(s)}
{1+G_A(s)G_E(s)G_G(s)H(s)}
$$

## Simulation Outputs

The MATLAB program generates the following outputs:

1. **Open-loop transfer function** — represents the combined amplifier, exciter, and generator dynamics.
2. **Closed-loop transfer function** — represents the complete AVR system with sensor feedback.
3. **Stability analysis** — determines whether the closed-loop system is stable by examining its poles.
4. **Step-response plot** — displays the terminal voltage response to a unit-step reference input.
5. **Performance analysis** — calculates rise time, settling time, overshoot, final voltage, and steady-state error.
6. **Amplifier gain comparison** — compares the responses for \(K_a=2,\ 5,\ 10\).
7. **Performance comparison table** — presents stability and transient-response measurements for each gain.
8. **Pole-zero map** — visualises the closed-loop system's poles and zeros.

## Expected Results

For the baseline amplifier gain \(K_a=10\), the theoretical steady-state gain is:

$$
V_{\infty}=\frac{10}{1+10}=0.9091\text{ p.u.}
$$

The corresponding steady-state error for a unit-step reference is:

$$
e_{ss}=\left|1-0.9091\right|\times100
$$

$$
e_{ss}\approx9.09\%
$$

The simulation compares the transient response and steady-state tracking performance at different amplifier gains. The numerical rise time, settling time, and overshoot are obtained directly from MATLAB.
<img width="799" height="600" alt="image" src="https://github.com/user-attachments/assets/4320c0a8-78d5-40d3-ba12-ef0f4e919ff7" />
<img width="799" height="599" alt="image" src="https://github.com/user-attachments/assets/6a61dc95-c1dd-4eb7-8aa6-78b00933d7be" />
<img width="799" height="600" alt="image" src="https://github.com/user-attachments/assets/f1479e21-915d-4bff-b640-328a2640fe22" />




## Technologies Used

* MATLAB
* Control System Toolbox
* Transfer Function Modelling
* Closed-Loop Control Systems
* Time-Domain Response Analysis
* Stability and Pole-Zero Analysis

## Applications

* Synchronous generator voltage regulation
* Power-system excitation control studies
* Feedback control-system analysis
* Engineering modelling and simulation
* Control-system performance evaluation

## Limitations

This project uses a simplified linear AVR model with first-order component dynamics. It does not include all the nonlinear characteristics, excitation limits, saturation effects, or detailed synchronous-generator dynamics found in practical systems.

## Conclusion

The project demonstrates how MATLAB can be used to model, simulate, and analyse an AVR control system. It illustrates the relationship between amplifier gain, steady-state voltage regulation, transient response, and closed-loop stability.

The results provide a foundation for further investigation into PI controllers, controller tuning, frequency-response analysis, and advanced excitation-system modelling.
