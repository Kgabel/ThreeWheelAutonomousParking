# Automatic Parallel Parking System for Three-Wheeled Tadpole Configuration

This project implements an **automatic parallel parking system** for a **three-wheeled tadpole configuration vehicle** with **two wheels at the front** and **one at the rear**. The system includes **path planning**, **path tracking**, and **parallel parking** functionalities. The environment has been updated to include **12 parking spaces**.

## Features

- **Environment Setup**: Designed using OpenCV to visualize obstacles and agent movement.
- **Path Planning**: Utilizes **A* algorithm** and **B-spline interpolation** for path finding and smoothing.
- **Path Tracking**: Based on a kinematic model with **Model Predictive Control (MPC)** for speed and steering.
- **Parallel Parking**: Vehicle performs parallel parking based on predefined rules and equations.

### Modified Features:
- **Three-Wheeled Vehicle**: Adapted for tadpole configuration (two wheels in the front, one at the rear).
- **Updated Parking Spaces**: Environment now features **12 parking spaces**.

## Vehicle Kinematic Model

The kinematic model for the vehicle is based on the following equations:

- \( \dot{x} = v \cdot \cos(\psi) \)
- \( \dot{y} = v \cdot \sin(\psi) \)
- \( \dot{v} = a \)
- \( \dot{\psi} = \frac{v \cdot \tan(\delta)}{L} \)

Where:
- \( x \), \( y \): Position
- \( v \): Velocity
- \( \psi \): Yaw angle
- \( a \): Acceleration
- \( \delta \): Steering angle
- \( L \): Wheelbase

### Control

The system uses **Model Predictive Control (MPC)** for controlling the vehicle's speed and steering. The MPC optimizes the control inputs to guide the vehicle along the planned path, ensuring smooth and efficient navigation.

## Automatic Parking

Parallel parking involves several key steps:

1. **Finding the Parking Spot**: The agent first identifies the optimal parking spot.
2. **Arriving Angle**: The arriving angle is computed to determine the vehicle's orientation as it approaches the parking spot.
3. **Ensure1 and Ensure2**:
    - **Ensure1**: A coordinate chosen based on the arriving angle.
    - **Ensure2**: A final coordinate where the parking maneuver is completed, planned using two circle equations to ensure the vehicle parks correctly.

The agent uses **MPC** to control the vehicle as it maneuvers from **Ensure1** to **Ensure2** for successful parking.


## How to Run

To set up the project, clone the repository and install dependencies:
```bash
https://github.com/Kgabel/ThreeWheelAutonomousParking.git
cd Automatic-Parking
pip install -r requirements.txt
python main_autopark.py --x_start 0 --y_start 90 --psi_start 0 --parking 4
```

## References
The original work and article on automatic parallel parking can be found on [Towards Data Science](https://towardsdatascience.com/automatic-parallel-parking-system-including-path-planning-path-tracking-and-parallel-parking-in-a-ece780b2e8e0).
