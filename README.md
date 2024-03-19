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

- `rviz`: For 3D robotic visualization.
- `urdf`: To parse URDF (Unified Robot Description Format) files.
- `xacro`: An XML macro language for generating URDF files.
- `gazebo_ros`: For integrating the Gazebo simulator with ROS.
- `robot_state_publisher`: To publish the state of the robot to the rest of the ROS ecosystem.
- `joint_state_publisher`: For publishing joint state values for the robot.
- `diagnostic_updater`: Provides a standardized interface for diagnostic information (used with the Xbox controller).
- `ros_control` and `ros_controllers`: To implement and manage robot controllers with ROS.
