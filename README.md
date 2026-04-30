<div align="center">

# ⚙️ DC Motor Speed Control

### MATLAB/Simulink and STM32-based DC motor modeling, PWM control, and closed-loop speed regulation

![MATLAB](https://img.shields.io/badge/MATLAB-Simulation-orange?style=for-the-badge&logo=mathworks)
![Simulink](https://img.shields.io/badge/Simulink-Control%20Model-blue?style=for-the-badge)
![STM32](https://img.shields.io/badge/STM32-Embedded%20Control-03234B?style=for-the-badge&logo=stmicroelectronics)
![Control Systems](https://img.shields.io/badge/Control%20Systems-DC%20Motor%20Speed%20Control-success?style=for-the-badge)

</div>

---

## 📌 Overview

This project presents a complete **DC motor speed control system** using **MATLAB/Simulink** for modeling and simulation, together with an **STM32 implementation package** for embedded motor control. The work focuses on understanding the dynamic behavior of a DC motor, generating PWM-based actuation, and designing a closed-loop control structure to regulate motor speed.

The repository includes:

- A MATLAB parameter file for the DC motor model
- Simulink models for motor modeling, PWM control, and closed-loop speed control
- An STM32 archive containing the embedded implementation files
- A final project report documenting the design and results

---

## 🎯 Project Goals

The main objectives of this project are:

- Model the electrical and mechanical behavior of a DC motor
- Simulate motor response in MATLAB/Simulink
- Design PWM-based speed control
- Implement closed-loop feedback control for speed regulation
- Prepare the project for embedded deployment using STM32
- Compare and document system behavior through a final report

---

## 🧠 System Concept

A DC motor speed control system adjusts the input voltage applied to the motor in order to control its angular speed. In practical systems, this is commonly achieved using **Pulse Width Modulation (PWM)** and a feedback controller.

The typical closed-loop structure is:

```text
Reference Speed ──► Controller ──► PWM Driver ──► DC Motor ──► Speed Output
      ▲                                                        │
      └────────────────────── Feedback Sensor ◄────────────────┘
```

The controller compares the desired speed with the measured speed and adjusts the PWM duty cycle to reduce the speed error.

---

## ⚙️ Motor Parameters

The MATLAB parameter file defines the main motor and load parameters used in the simulation:

| Parameter | Meaning | Value |
|---|---:|---:|
| `Va` | Armature voltage | `240 V` |
| `Ra` | Armature resistance | `0.78 Ω` |
| `La` | Armature inductance | `0.016 H` |
| `B` | Viscous friction coefficient | `0.02` |
| `J` | Moment of inertia | `5` |
| `T1` | Load torque | `30` |
| `K` | Motor constant | `1.4` |

These parameters are used to describe the motor dynamics and evaluate its speed response under different control conditions.

---

## 🧮 DC Motor Mathematical Model

A simplified separately excited DC motor can be described using the following equations:

### Electrical equation

```math
V_a(t) = R_a i_a(t) + L_a \frac{di_a(t)}{dt} + e_b(t)
```

### Back EMF equation

```math
e_b(t) = K \omega(t)
```

### Mechanical equation

```math
J \frac{d\omega(t)}{dt} + B\omega(t) = K i_a(t) - T_L
```

Where:

- `Va` is the armature voltage
- `Ra` is the armature resistance
- `La` is the armature inductance
- `ia` is the armature current
- `eb` is the back electromotive force
- `J` is the motor inertia
- `B` is the viscous friction coefficient
- `K` is the motor constant
- `ω` is the angular velocity
- `TL` is the load torque

---

## 🔌 STM32 Implementation

The repository also includes `stm32.rar`, which contains files related to the embedded implementation of the motor control system.

The STM32 part is intended to connect the control concept from simulation to a microcontroller-based environment. Depending on the extracted project structure, it may include configuration files, source code, peripheral setup, PWM generation, or feedback processing.

Suggested STM32 workflow:

1. Extract `stm32.rar`
2. Open the extracted project in STM32CubeIDE or a compatible IDE
3. Check the configured peripherals, especially PWM timer outputs and feedback input channels
4. Build the project
5. Flash it to the selected STM32 board
6. Test the motor driver and feedback loop carefully with a suitable power supply and motor driver circuit

---

## 📊 Expected Results

The project demonstrates how a DC motor speed can be controlled using a feedback-based control structure. The expected outcomes include:

- Simulated DC motor dynamic response
- PWM signal generation for motor actuation
- Closed-loop speed tracking
- Reduced speed error compared with open-loop operation
- Embedded implementation path using STM32

---

## 🛠️ Technologies Used

| Category | Tools / Concepts |
|---|---|
| Modeling | MATLAB, Simulink |
| Control | Closed-loop control, feedback control, PWM |
| Embedded System | STM32 |
| Electrical System | DC motor model, armature circuit, back EMF |
| Documentation | Final project report |

---

## 💡 Key Learning Outcomes

Through this project, the following topics are practiced:

- DC motor dynamic modeling
- Electrical and mechanical system equations
- PWM-based motor actuation
- Closed-loop speed regulation
- MATLAB/Simulink simulation workflow
- Embedded control implementation using STM32
- Control system documentation and reporting

---

## 📌 Applications

DC motor speed control is widely used in:

- Robotics
- Industrial automation
- Electric vehicles
- Conveyor systems
- CNC machines
- Smart mechatronic systems
- Embedded motor control platforms

---

## 👤 Author

**Mohammad Barabadi**  
GitHub: [@mohammadbrd](https://github.com/mohammadbrd)

---

## 📄 License

No license file is currently included in this repository. If you plan to reuse or distribute this project, please contact the author or add an appropriate open-source license.

---

<div align="center">

### ⭐ If you find this project useful, consider starring the repository.

</div>
