# Aggressive Maneuver Stabilization and Control (AMSC)

This repository is dedicated to the development and implementation of a robust quaternion-based control system for quadrotor UAVs. Specifically designed for aggressive maneuvers, this system ensures global stability and precise attitude tracking in dynamic environments. Leveraging advanced geometric tracking control on SE(3) and quaternion-based attitude control, the project addresses challenges like gimbal lock, nonlinear dynamics, and high-rotation maneuvers.

---

## Project Motivation

Conventional control techniques often fail during aggressive UAV maneuvers due to limitations like singularities, noise sensitivity, and computational complexity. This project aims to:

- Overcome these limitations by integrating quaternion-based control for robust attitude tracking.
- Develop a hybrid control system that combines geometric and quaternion-based approaches.

This work has applications in aerial robotics for **search and rescue**, **surveillance**, and **industrial inspection**.

---

## Features

- **Hybrid Control Framework**: Combines **Geometric Tracking Control** on SE(3) for position and altitude tracking and **Quaternion-Based Attitude Control** for orientation stabilization.
- **Simulation of Aggressive Maneuvers**: Includes scenarios such as 360-degree flips and helical trajectories.
- **High Precision Tracking**: Achieves minimal position and velocity errors even during aggressive maneuvers.

---

## Key Algorithms

1. **Geometric Tracking Control on SE(3)**:
   - Operates directly on nonlinear manifolds.
   - Ensures global stability and avoids singularities.

2. **Quaternion-Based Attitude Control**:
   - Singularities-free orientation control using compact quaternion representation.
   - Computationally efficient and precise during high-rotation dynamics.

3. **Hybrid Approach**:
   - Combines the strengths of both approaches to balance altitude and attitude control.

---

## Implementation Details

- **Platform**: MATLAB/Simulink for simulation and control algorithm development.
- **Test Scenarios**: Includes trajectory tracking for:
  - **Flip Maneuver**: Large rotational displacements over a short duration.
  - **Helical Trajectory**: Smooth circular motion with progressive ascent.
- **Control Inputs**:
  - Altitude Controller: Generates thrust \( F \).
  - Attitude Controller: Computes torque using quaternion-based feedback.

---

## Project Structure

### Main Directories and Files:
- **`PIDController`**
  - Contains the implementation of the PID controller.
  - File: `pid_euler_control.mlx` - MATLAB Live Script for the Euler-based PID control implementation.

- **`geometricTrackingController`**
  - Implements the geometric tracking controller with supporting functions.
  - Files:
    - `geometricTrackingControl.mlx`: Main MATLAB Live Script for the geometric tracking controller.

      **Helper Functions**
       - `RPYToRot_ZXY.m`: Converts roll, pitch, and yaw to a rotation matrix.
       - `flippp.mlx`: Helper script for flipping transformations.
       - `hat_map.m`, `vec_cross.m`, `vec_dot.m`, `vee_map.m`: Supporting MATLAB scripts for vector and matrix operations.
       - `helical.mlx`: Script for helical motion dynamics.

- **`proposedController`**
  - Implements a proposed controller.
  - Files:
    - `Proposed_Controller.mlx`: MATLAB Live Script for the proposed controller.

- **`quaternionController`**
  - Implements a quaternion-based controller.
  - Files:
    - `Drone_quaternion.mlx`: MATLAB Live Script for the quaternion-based control.

- **Other Files**
  - `Final Report.pdf`: Detailed project report.
  - `LICENSE`: Licensing information for this repository.
  - `README.md`: The current documentation file.

---

## Navigating the Files

1. **Start with the `Final Report.pdf`**  
   Review this file for a comprehensive understanding of the project objectives, methodologies, and results.

2. **Explore Controller Implementations**  
   Navigate to the respective controller directories (`PIDController`, `geometricTrackingController`, `proposedController`, `quaternionController`) based on your interest:
   - Open the `.mlx` files in MATLAB for interactive scripts and step-by-step analysis.
   - Use supporting `.m` files as needed to understand or modify the computations.

3. **Understanding the Supporting Files**  
   Supporting scripts in `geometricTrackingController` (e.g., `hat_map.m`, `vec_cross.m`) provide auxiliary functionalities for vector and matrix operations, which are crucial for geometric tracking.

4. **Experimenting and Testing**  
   Open the MATLAB Live Scripts (`.mlx`) in MATLAB:
   - Run the scripts interactively to observe the controller performance.
   - Modify the parameters or functions to customize the controllers as needed.

---

## Usage Instructions


### Steps:
1. Clone the repository:
   ```bash
   git clone https://github.com/Vezz-084/Aggressive-Maneuver-Stabilization-And-Control.git
   ```
2. Open MATLAB and navigate to the cloned repository directory.
3. Access the desired script or function:
   - Open `.mlx` files in MATLAB for interactive execution.
   - Edit `.m` files for customizations.

4. Run the scripts to test the controllers and analyze the results.

---


## Acknowledgments

This project builds upon foundational works such as:
- "Full Quaternion-Based Attitude Control for a Quadrotor" (Fresk and Nikolakopoulos, 2013).
- "Geometric Tracking Control of a Quadrotor UAV on SE(3)" (Lee et al., 2010).

