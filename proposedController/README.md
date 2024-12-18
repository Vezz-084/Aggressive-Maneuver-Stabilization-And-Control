### Hybrid Controller

#### Overview
The **Hybrid Controller** combines the strengths of the Quaternion-Based Controller and the Geometric Tracking Controller. It ensures robust altitude and attitude tracking during aggressive UAV maneuvers.

#### Features
- **Altitude Control**: Utilizes geometric tracking on SE(3) for thrust computation.
- **Attitude Control**: Leverages quaternion-based dynamics for torque computation.
- **Disturbance Resistance**: Robust performance under dynamic conditions.

#### Key Algorithms
- **Altitude Controller**:
  - ![equation](https://latex.codecogs.com/svg.image?F=-k_x%5Ccdot%20e_x-k_v%5Ccdot%20e_v&plus;m%5Ccdot%5Cddot%7Bx%7D_d&plus;m%5Ccdot%20g%5Ccdot%20e_3)  
- **Attitude Controller**:
  - ![equation](https://latex.codecogs.com/svg.image?%5Ctau=-K_q%5Ccdot%20q_%7B%5Ctext%7Berr%7D%7D-K_%5Comega%5Ccdot%5Comega)

#### Applications
- Complex UAV operations involving aggressive maneuvers.
- High-precision tasks requiring altitude and attitude coordination.
