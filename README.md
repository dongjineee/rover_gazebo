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

### ROS 필요 패키지
- `rviz`
- 'urdf'
- 'xacro'
- 'gazebo'
- 'robot-state-publisher'
- 'joint-state-publisher'
- 'diagnostic-updater' # xbox controller
- 'ros-controllers'
