# 🤖 ROS2 Mobile Robot Simulation


A beginner-friendly ROS2 project focused on designing and simulating a custom mobile robot using URDF/Xacro and launching it in Gazebo and RViz.

---

# 📖 Project Overview

This project demonstrates how to build a complete custom robot simulation pipeline in ROS2 Humble by creating a robot model from scratch and deploying it into a simulation environment.

The project includes:

- Custom robot design using URDF/Xacro
- Robot visualization in RViz
- Gazebo simulation environment
- ROS2 launch configuration
- Modular package architecture
- Velocity control using ROS topics

---

# 🎥 Demo

## Live Demo Video

https://github.com/Pavan-rai/robot_simulation_project/blob/main/demo.mp4

---

# 🛠 Tech Stack

- ROS2 Humble
- C++
- Python
- URDF
- Xacro
- Gazebo
- RViz2
- Ubuntu Linux

---

# 📦 Packages

## my_robot_description

Contains robot model-related files:

- URDF/Xacro files
- Robot meshes
- Configuration files

Responsibilities:

- Define robot links and joints
- Configure robot structure
- Handle visualization setup

---

## my_robot_bringup

Contains launch configurations:

- Gazebo launch files
- RViz launch files
- Robot spawning scripts

Responsibilities:

- Launch robot simulation
- Spawn robot into Gazebo
- Initialize visualization pipeline

---

# ✨ Features

- Custom mobile robot creation
- Modular ROS2 package architecture
- Gazebo simulation deployment
- RViz visualization
- Velocity control using topics
- Easy extension for navigation and perception

---

# 🏗 Project Structure

```bash
robot_simulation_project/
│
├── my_robot_description/
│   ├── urdf/
│   ├── meshes/
│   └── config/
│
├── my_robot_bringup/
│   ├── launch/
│   └── worlds/
│
├── build/
├── install/
├── log/
│
├── demo.mp4
└── README.md
```

---

# 🚀 How to Run

Build workspace:

```bash
cd ~/robot_simulation_project

colcon build

source install/setup.bash
```

Launch simulation:

```bash
ros2 launch my_robot_bringup my_robot_gazebo.launch.xml
```

---

# 🎮 Robot Control

Move the robot manually using ROS2 topic publishing.

### Forward motion

```bash
ros2 topic pub /cmd_vel geometry_msgs/msg/Twist "{linear: {x: 2.0}}"
```

### Rotate robot

```bash
ros2 topic pub /cmd_vel geometry_msgs/msg/Twist "{angular: {z: 1.0}}"
```

### Move and rotate simultaneously

```bash
ros2 topic pub /cmd_vel geometry_msgs/msg/Twist "{linear:{x:1.0}, angular:{z:0.5}}"
```

### Stop robot

```bash
ros2 topic pub /cmd_vel geometry_msgs/msg/Twist "{}"
```

---

# 📚 ROS2 Concepts Demonstrated

- Publisher / Subscriber communication
- Robot simulation
- URDF robot modeling
- Xacro modular design
- Gazebo integration
- RViz visualization
- Topic-based robot control

---

# 🔮 Future Improvements

- Add autonomous navigation
- Integrate SLAM
- Obstacle avoidance
- Camera and LiDAR sensors
- Navigation2 stack
- Object detection with YOLO

---

# 👨‍💻 Author

**Pavan Rai**

GitHub: https://github.com/Pavan-rai

If you found this useful, consider giving the repository a ⭐
