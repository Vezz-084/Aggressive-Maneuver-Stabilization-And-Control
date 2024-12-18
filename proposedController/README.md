### Hybrid Controller

#### Overview
The **Hybrid Controller** combines the strengths of the Quaternion-Based Controller and the Geometric Tracking Controller. It ensures robust altitude and attitude tracking during aggressive UAV maneuvers.

#### Features
- **Altitude Control**: Utilizes geometric tracking on \( SE(3) \) for thrust computation.
- **Attitude Control**: Leverages quaternion-based dynamics for torque computation.
- **Disturbance Resistance**: Robust performance under dynamic conditions.

#### Key Algorithms
- **Altitude Controller**:
  - \( F = -k_x \cdot e_x - k_v \cdot e_v + m \cdot \ddot{x}_d + m \cdot g \cdot e_3 \)
- **Attitude Controller**:
  - \( \tau = -K_q \cdot q_{\text{err}} - K_\omega \cdot \omega \)
- Hybrid integration for simultaneous trajectory and orientation tracking.

#### Applications
- Complex UAV operations involving aggressive maneuvers.
- High-precision tasks requiring altitude and attitude coordination.
