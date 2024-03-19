# ROS packages for Curio - a Sawppy Rover

## Introduction
This is a collection of ROS software packages to control a version of [Roger Chen's Sawppy Rover](https://github.com/roger-random/Sawppy_Rover). These packages are intended to help builders of Roger's Sawppy up and running on ROS while staying faithful to the original design using LX-16A servo motors. This presents some challenges with getting reliable odometry which we address with an encoder filter that identifies when the encoder position is outside its valid range.

## Overview
There are a number of ROS packages to control the rover, visualise it in rviz, and simulate it in Gazebo.

- `ackermann_drive_controller`: a 6 wheel, 4 steering controller consistent with the `ros_control` framework.
- `curio_base`: hardware drivers and a ROS base controller node subscribing to `geometry_msgs/Twist` on `/cmd_vel`.
- `curio_bringup`: a set of launch files for bringing up the rover nodes.
- `curio_control`: configuration and launch files using the `ros_control` framework.
- `curio_description`: a URDF/xacro model for the robot using STL files from the Sawppy CAD model.
- `curio_gazebo`: configuration and launch files for spawning the rover in Gazebo with ROS control.
- `curio_navigation`: configuration and launch files for the ROS navigation stack.
- `curio_teleop`: a teleop node for interpreting PWM signals from a RC unit and publishing to `/cmd_vel`.
- `curio_viz`: configuration and launch files for loading the robot model into `rviz`.

For more detail see the sections below.

## Installation

// Provide a step-by-step guide on how to install the packages.

## Usage

// Describe how to use the packages, any important commands, and how to run the software.

## Contributing

// Explain how others can contribute to the project. Include guidelines for code contributions, how to submit issues, and so forth.

## License

// Specify the license under which the project is made available.

