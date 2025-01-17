# MATLAB/Simulink Medical CO₂ Insufflator

This repository contains the replication and implementation of the MATLAB/Simulink medical CO₂ insufflator system described in the 2020 IEEE 5th Middle East and Africa Conference on Biomedical Engineering (MECBME). The system includes a PID-controlled DC motor and a PPR valve, as well as a nonlinear abdominal model. The integration of these models allows for system testing, optimization, and performance validation in a virtual environment.

## Features
- **PID Controller Auto-Tuning**: Automatically tunes the PID parameters to achieve an optimal balance between minimum response time and smooth trajectory response.
- **Pressure Control**: Simulates and regulates CO₂ pressure from high-pressure units (HPU) to low-pressure units (LPU) with precise control.
- **Temperature Monitoring**: Models and adjusts CO₂ gas temperature to approximately 37°C before abdominal cavity entry.
- **Flow and Volume Measurement**: Simulates CO₂ flow rates and delivers accurate gas volumes to the abdominal cavity.

## Key Components
1. **High-Pressure Unit (HPU)**: Monitors the pressure inside the CO₂ cylinder (~50 bar) using the P1 sensor.
2. **Low-Pressure Unit (LPU)**: Regulates pressure to the surgeon-defined setpoint (e.g., 15 mmHg) using the P2 sensor.
3. **Temperature Sensors (T1 & T2)**: Ensure proper heating of CO₂ gas prior to use.
4. **Flow Sensors**: Simulate CO₂ flow stability over time.
5. **CO₂ Volume Simulation**: Models the constant gas volume delivered into the abdominal cavity (~1.2 liters).

## Simulink Models
- **PID Controller**: Optimized for DC motor and PPR valve control.
- **Abdominal Model**: A nonlinear simulation that accounts for abdominal cavity behavior (excluding orifice leakage and blood absorption).

## Advantages
- Computationally evaluates performance without risking physical components.
- Speeds up the transition from design to final product development.

## Results
### Figures
- **PPR Output**: Improved response curve using MATLAB's auto-tuner.
- **Pressure**: Sensor readings of HPU (P1) and LPU (P2).
- **Temperature**: Gas temperature at T1 (after heating) and T2 (before cavity entry).
- **Flow**: Stabilized CO₂ flow rates.
- **Volume**: Delivered CO₂ gas volume reaching a constant value.

## Acknowledgments
This project was sponsored by **Ingenious Medical**. Special thanks to **Eng. Hassan Wehbi**, Development Manager at Ingenious Medical, for his valuable inputs and support.

## How to Use
1. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/MATLAB-Simulink-Medical-CO2-Insufflator.git
