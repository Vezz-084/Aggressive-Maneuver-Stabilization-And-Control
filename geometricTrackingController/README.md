### Geometric Tracking Controller

#### Overview
The **Geometric Tracking Controller** operates on the \( SE(3) \) manifold, combining translational and rotational control for quadrotor UAVs. It ensures global stability and precise trajectory tracking, avoiding the limitations of Euler angles.

#### Features
- **Nonlinear Control on \( SE(3) \)**: Directly tracks position and orientation on nonlinear manifolds.
- **Singularity Avoidance**: Eliminates issues such as gimbal lock.
- **Robust to Aggressive Maneuvers**: Ideal for high-speed and large-rotation trajectories.

#### Key Algorithms
- Position and velocity error dynamics:
  - ![equation](https://latex.codecogs.com/svg.image?e_x=x-x_d,%5Cquad%20e_v=%5Cdot%7Bx%7D-%5Cdot%7Bx%7D_d)
- Control law for thrust:
  - ![equation](https://latex.codecogs.com/svg.image?F=-k_x%5Ccdot%20e_x-k_v%5Ccdot%20e_v&plus;m%5Ccdot%5Cddot%7Bx%7D_d&plus;m%5Ccdot%20g%5Ccdot%20e_3)
- Rotational dynamics using the desired rotation matrix.
