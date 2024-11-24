

---

# Mini Tracker Robot: Light Spot Tracking System

This project implements a **Neural Network-based control system** for a mobile robot designed to follow a light source. The system leverages MATLAB and Simulink for simulation and neural network training.

---

## Table of Contents

1. [Introduction](#introduction)
2. [Project Features](#project-features)
3. [System Implementation](#system-implementation)
4. [Simulation and Results](#simulation-and-results)
5. [Files and Structure](#files-and-structure)
6. [Usage](#usage)
7. [Future Enhancements](#future-enhancements)

---

## Introduction

The objective is to design a two-wheeled robot equipped with light sensors to track a light source using a neural network. The system processes sensor inputs and calculates appropriate wheel velocities to guide the robot towards the light spot. This approach showcases adaptability to varying light conditions and positions, emphasizing neural network-based control systems.

---

## Project Features

- **Neural Network Controller**: Processes sensor data and generates control signals.
- **Dynamic Adaptation**: Responds to varying light intensities and locations.
- **MATLAB/Simulink Integration**: Simulates real-world behavior.
- **Robust Design**: Ensures adaptability to disturbances and dynamic environments.

---

## System Implementation

### 1. Neural Network Training
- **Input Data (P)**: Generated using sensor readings.
- **Target Data (T)**: Represents desired wheel velocities.
- **Training Algorithm**: Feed-forward network with supervised learning.

Key MATLAB Functions:
- **`sensor_model.m`**: Simulates sensor readings.
- **`velocity_estimator.m`**: Calculates wheel velocities.
- **`trainin_net.m`**: Trains the neural network.

### 2. Prediction and Control
- **Controller**: Uses trained neural network to predict wheel velocities.
- **Relative Location Calculation**: Determines the angle and distance between the robot and the light source.

Key MATLAB Functions:
- **`relative_location.m`**: Calculates light's relative position.
- **`control_net.m`**: Executes velocity predictions.

### 3. Simulation
- Simulated in Simulink using `MiniTracker_Model.slx`.
- Multiple light positions tested to verify accuracy.

---

## Simulation and Results

- **Test Scenarios**:
  - Position 1: [25, -10]
    ![1](https://github.com/user-attachments/assets/0de9301a-1a08-411c-8332-c5d76ae0ce08)
  - Position 2: [10, 10]
   ![2](https://github.com/user-attachments/assets/ccb674d7-b445-4b26-9858-1abcac9e0cf3)
  - Position 3: [-10, 10]
    ![3](https://github.com/user-attachments/assets/25db96dd-4ba6-4f31-84c3-e4b48cdd796e)

- **Performance**:
  - Successfully tracked light positions with high accuracy.
  - Minor deviations due to limited training data and robot dynamics.

**Visualization**: Simulations demonstrate the robot moving towards the light source under various conditions.

---

## Files and Structure

- **MATLAB Scripts**:
  - `sensor_model.m`: Sensor input generation.
  - `velocity_estimator.m`: Calculates wheel velocities.
  - `relative_location.m`: Computes light-source position relative to the robot.
  - `trainin_net.m`: Trains the neural network.
  - `control_net.m`: Predicts velocities using the trained network.
- **Simulink File**:
  - `MiniTracker_Model.slx`: System simulation.

---

## Usage

1. **Setup**:
   - Ensure MATLAB and Simulink are installed.
   - Load all MATLAB scripts and Simulink models into your workspace.

2. **Train the Model**:
   ```matlab
   run('trainin_net.m');
   ```

3. **Simulate**:
   - Open `MiniTracker_Model.slx` in Simulink.
   - Configure light position and run the simulation.

4. **Analyze**:
   - Check simulation results for trajectory accuracy.

---

## Future Enhancements

- **Expand Training Data**: Increase dataset size for improved precision.
- **Optimize Dynamics**: Refine wheel mechanics to reduce deviations.
- **Real-world Testing**: Transition from simulation to physical implementation.

---

## Contributors

- **Jean Junior Maldini Jiokeng I Toko** (ID: 159010)
- **Seid Fikreselassie Eshetu** (ID: 162943)

---

