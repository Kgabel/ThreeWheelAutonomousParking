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

## Installation

To set up the project, clone the repository and install dependencies:
```bash
git clone https://github.com/yourusername/Automatic-Parking.git
cd Automatic-Parking
pip install -r requirements.txt
