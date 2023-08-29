## Cascaded PI Controller for Linear Servo Belt Drive System
# Project Description
This repository contains the code and documentation for a cascaded PI controller designed for a linear servo belt drive system, implemented using Simulink. The project employs the Parameter Estimation toolbox to estimate the system parameters.

The control system uses two PI controllers in a cascaded configuration to achieve precise and stable control of the belt drive system. The inner loop controller regulates the motor speed, while the outer loop controller controls the position of the belt. The design and tuning of the controllers are based on the system’s dynamic model and performance requirements.

# System Model
The system model is composed of three parts:

- Controller: The controller is a pair of cascaded PI controllers discretized at a 200 Hz sampling frequency.
- Linear Servo: The Linear Servo is composed of a deadzone block followed by a linear state space model, also discretized at the stated frequency.
- Data Acquisition System: The data acquisition system simulates the effect of the encoder’s resolution on the control system’s performance.
# Repository Contents
The repository contains several files, including:

- Sensor data file: This file contains the sensor data that was used for parameter estimation.
- M-script file: This file contains the system parameters initialization as well as the Simulink model itself.

# Project Steps

- Parameter Estimation
The sensor readings were obtained by driving the motor as an open-loop, changing the input duty cycle using a potentiometer. It was then left to estimate the system parameters using the sensor data. This was done using the Parameter Estimation toolbox in Simulink. The sensor data was imported into Simulink and used to estimate the system parameters.

- Controller Tuning
The cascaded controller could not be reliably tuned using the Control System Designer toolbox due to the large deadzone present in the system. Instead, it was tuned manually using trial and error, with a starting point approximating the system as a first-order transfer function with a time constant measured from its step response.

- Simulation and Testing
The final step was to simulate and test the control system using Simulink. The simulation results were analyzed to verify that the control system met its performance requirements.

![untitled](https://github.com/omarequalmars/LinearServoCascadedPI/assets/90857121/4ec06f2f-9f0c-4fbc-a964-10c70393e610)


# Documentation
The repository includes detailed documentation on its system model, controller design, simulation results, and parameter estimation. This documentation provides a comprehensive overview of this project and can be used as a reference for anyone interested in control systems design and implementation using Simulink.
