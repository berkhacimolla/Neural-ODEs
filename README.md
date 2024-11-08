# Neural ODE Models: Oscillatory and Lorenz Systems

This project contains two implementations of Neural Ordinary Differential Equations (ODEs) using PyTorch. The goal is to simulate and predict dynamics in two different systems: a simple oscillatory system and a chaotic Lorenz system.

## Project Structure

The project is divided into two main scripts:

1. **Oscillatory System (Spring-Mass System)**
    - Models a 1D harmonic oscillator using a simple spring-mass system.
    - The system is parameterized by spring constant \( k \) and mass \( m \), which are learned from generated data.
    - Initial position and velocity are also learned as parameters.
    - The model generates synthetic data by solving the equations of motion and then trains the neural network to predict the system's trajectory.

2. **Lorenz System (Chaotic System)**
    - Implements the Lorenz system of equations to model a chaotic attractor.
    - Uses sequences of data to predict future states of the Lorenz attractor over an extended time range.
    - Captures the complex and sensitive dependency on initial conditions characteristic of chaotic systems.

## Features

- **Data Generation**: Each script includes functions for generating synthetic data based on analytical solutions of the respective systems.
- **Model Architecture**: Both models use a neural network to approximate derivatives in the systems. They incorporate the `odeint` function for integrating ODEs over time.
- **Training Process**: Models are trained to minimize the difference between predicted and true trajectories, with early stopping to prevent overfitting.
- **Visualization**:
  - **Trajectories**: Plots comparing predicted and true values over time.
  - **Phase Space**: Visualization of position vs. velocity (Oscillatory System) or x-y-z trajectories (Lorenz System).
  - **Loss Curve**: Tracks the loss over epochs to monitor convergence.

## Getting Started

1. **Requirements**: Install the required libraries, primarily `torch` and `matplotlib`.
2. **Run the Scripts**: 
   - **Oscillatory System**: Run the first script to simulate and train the spring-mass model.
   - **Lorenz System**: Run the second script for the Lorenz attractor, adjusting sequence length and batch size if needed.
3. **View Outputs**: Each script will produce visualizations for model performance and learned dynamics.


