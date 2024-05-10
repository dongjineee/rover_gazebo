# ROS packages for JPL Open Source Rover Gazebo Simulation

## Overview
The following ROS packages are included to visualize the rover in rviz and simulate its operations in Gazebo:

- `rviz.launch`: Launches a package for observing the rover in rviz, providing real-time visualization of its movements and sensor data.
- `empty_world.launch`: Deploys the rover within the Gazebo simulation environment, creating a virtual testing ground for rover operations.
- `controller.launch`: Initializes the control system for the rover, setting the stage for user interaction through various input devices.

## Dependencies

### Linux
- Operating System: Ubuntu 20.04.06 LTS &&  Ubuntu 22.04.06 LTS
- ROS Distribution: foxy && iron && humble
- Gazebo Version: 11.14.0

### Required ROS Packages
To fully utilize the capabilities of the rover simulation, the following ROS packages are necessary:

```bash
sudo apt install python3-colcon-common-extensions
sudo apt-get install ros-${ros-distro}-rviz2
sudo apt-get install ros-${ros-distro}-controller-manager
sudo apt-get install ros-${ros-distro}-robot-state-publisher
sudo apt-get install ros-${ros-distro}-joint-state-publisher
sudo apt-get install ros-${ros-distro}-joint-state-publisher-gui 
sudo apt-get install ros-${ros-distro}-gazebo-ros-pkgs
sudo apt-get install ros-${ros-distro}-trajectory-msgs
sudo apt-get install ros-${ros-distro}-velocity-controllers
sudo apt-get install ros-${ros-distro}-joint-trajectory-controller
sudo apt-get install ros-${ros-distro}-gazebo-ros2-control-demos
```

## Installation

### 버전 차이 주의 

## foxy 버전
```bash
    load_joint_state_controller = ExecuteProcess(
        cmd=['ros2', 'control', 'load_controller', '--set-state', 'start', 'joint_state_broadcaster'],
        output='screen'
    )

    # wheel_velocity_controller
    rover_wheel_controller = ExecuteProcess(
        cmd=['ros2', 'control', 'load_controller', '--set-state', 'start', 'wheel_controller'],
        output='screen'
    )

    # servo_controller
    servo_controller = ExecuteProcess(
        cmd=['ros2', 'control', 'load_controller', '--set-state', 'start', 'servo_controller'],
        output='screen'
    )
```

## iron && humble 버전
```bash
    load_joint_state_controller = ExecuteProcess(
        cmd=['ros2', 'control', 'load_controller', '--set-state', 'active', 'joint_state_broadcaster'],
        output='screen'
    )

    # wheel_velocity_controller
    rover_wheel_controller = ExecuteProcess(
        cmd=['ros2', 'control', 'load_controller', '--set-state', 'active', 'wheel_controller'],
        output='screen'
    )

    # servo_controller
    servo_controller = ExecuteProcess(
        cmd=['ros2', 'control', 'load_controller', '--set-state', 'active', 'servo_controller'],
        output='screen'
    )
```


### Create and configure a workspace
Source your ROS installation:
```bash
source /opt/ros/foxy/setup.bash
```
build the osr-gazebo packages:
```bash
cd ~/osr-rover-code/ROS/osr_gazebo
colcon build
source ~/osr-rover-code/ROS/osr_gazebo/install/setup.bash
```
## Visualisation

### `rover_rviz`

This package includes launch and rviz configuration files for visualising the rover.

To view the rover in rviz and manually control the joints, execute the following command:

```bash
ros2 launch osr_gazebo rviz.launch.py
```
![image](https://github.com/dongjineee/rover_gazebo/assets/150753899/f49548d0-8ecb-4b25-8ce6-bd643bb90b1a)

## Simulation

### `rover_simulation`

This package provides essential launch needed for the visualization of the rover within a simulation environment.

To launch the simulation along with the capability to manually control the joints, use the command:


```bash
ros2 launch osr_gazebo empty_world.launch.py
```
![image](https://github.com/dongjineee/rover_gazebo/assets/150753899/481e0aaf-6336-45e5-b138-49ee7df5e509)

### `rover_control`

To launch the simulation along with the capability to manually control the joints, use the command:
```bash
ros2 launch osr_gazebo controller.launch.py
```
Keyboard controller
```bash
ros2 run teleop_twist_keyboard teleop_twist_keyboard
```
## Note
- The control does not have specified linear and angular velocities. Therefore, it's necessary to add the maximum and minimum values for `cmd_vel` in the `motor_controller.cpp`.
- The ROS1::noetic version of gazebo simulation exists at https://github.com/dongjineee/rover_gazebo.
