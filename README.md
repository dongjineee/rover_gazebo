# ROS packages for JPL Open Source Rover Gazebo Simulation

## Introduction
This package suite is designed to bring the JPL Open Source Rover to life in a simulated environment using Gazebo. Inspired by [NASA JPL's Open Source Rover project](https://github.com/nasa-jpl/open-source-rover), these packages allow for visualization and control in a Gazebo simulation.

## Overview
The following ROS packages are included to visualize the rover in rviz and simulate its operations in Gazebo:

- `rover.launch`: Launches a package for observing the rover in rviz, providing real-time visualization of its movements and sensor data.
- `rover_gazebo.launch`: Deploys the rover within the Gazebo simulation environment, creating a virtual testing ground for rover operations.
- `controller.launch`: Initializes the control system for the rover, setting the stage for user interaction through various input devices.
- `rover_teleop_keyboard.launch`: A package that allows the user to maneuver the rover using keyboard inputs, ensuring precise and responsive control.
- `rover_teleop_xbox.launch`: Enables control of the rover via an Xbox controller, offering an intuitive and ergonomic option for navigation and operation.

## Dependencies

### Linux
- Operating System: Ubuntu 20.04.06 LTS
- ROS Distribution: Noetic
- Gazebo Version: 11.14.0

### Required ROS Packages
To fully utilize the capabilities of the rover simulation, the following ROS packages are necessary:

- `rviz`
- `urdf`
- `xacro`
- `gazebo_ros`
- `robot_state_publisher`
- `joint_state_publisher`
- `diagnostic_updater`
- `ros_control`

## Installation

### Create and configure a workspace
Source your ROS installation:
```bash
source /opt/ros/noetic/setup.bash
```
Source your ROS installation:
