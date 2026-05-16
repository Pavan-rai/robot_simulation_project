# ROS2 Mobile Robot Simulation

A beginner-level ROS2 project focused on designing and simulating a custom mobile robot using URDF/Xacro and launching it in Gazebo and RViz.

## Project Overview

This project demonstrates how to build a custom robot simulation pipeline in ROS2 Humble by creating a robot model from scratch and deploying it in a simulation environment.

The project includes:

- Custom robot design using URDF/Xacro
- Robot visualization in RViz
- Gazebo simulation environment
- ROS2 launch configuration
- Modular package structure for scalability

---
# 🎥 Demo

## Live Demo Video



## Tech Stack

- ROS2 Humble
- C++
- Python
- URDF
- Xacro
- Gazebo
- RViz2
- Linux (Ubuntu)

---x = -1.031316
   y = -1.504092

## Packages

### my_robot_description

Contains robot model-related files:

- URDF/Xacro files
- Robot meshes
- Robot configuration files

Responsibilities:

- Defines robot links and joints
- Configures robot physical structure
- Handles visualization setup

---

### my_robot_bringup

Contains launch configurations:

- Gazebo launch files
- RViz launch files
- Robot spawning scripts

Responsibilities:

- Launch robot simulation
- Spawn robot into Gazebo
- Initialize visualization pipeline

---

## Features

- Custom mobile robot creation
- Modular ROS2 package architecture
- Gazebo simulation deployment
- RViz visualization
- Easy package extension for navigation/perception

---

## How to Run

```bash
cd ~/robot_simulation_project
colcon build
source install/setup.bash
ros2 launch my_robot_bringup my_robot_gazebo.launch.xml

# 🎮 Robot Control

Move the robot manually using ROS2 topic publishing:

Forward motion:

```bash
ros2 topic pub /cmd_vel geometry_msgs/msg/Twist "{linear: {x: 2.0}}"
```

Rotate robot:

```bash
ros2 topic pub /cmd_vel geometry_msgs/msg/Twist "{angular: {z: 1.0}}"
```

Move and turn simultaneously:

```bash
ros2 topic pub /cmd_vel geometry_msgs/msg/Twist "{linear:{x:1.0},angular:{z:0.5}}"
```

Stop robot:

```bash
ros2 topic pub /cmd_vel geometry_msgs/msg/Twist "{}"


# 👨‍💻 Author

**Pavan Rai**

GitHub: https://github.com/Pavan-rai

If you found this useful, consider giving the repository a ⭐
```
