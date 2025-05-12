# Spot ROS 2 Gazebo Simulation

This repository contains a custom simulation of the **Boston Dynamics Spot robot** developed using **ROS 2** and **Gazebo**.

![Spot Robot in Gazebo](https://github.com/manoj5121/spot-ros2-gazebo-simulation/blob/master/Screenshot%20from%202025-05-12%2021-11-43.png?raw=true)

## Project Overview
The goal of this project is to simulate the behavior of the Spot robot in a Gazebo environment using ROS 2, enabling testing of basic movement, navigation, and control algorithms.

# Spot ROS 2 Gazebo Simulation

This repository contains a custom simulation of the **Boston Dynamics Spot robot** developed using **ROS 2** and **Gazebo**. The simulation integrates Spot's quadruped control framework and provides a realistic environment for testing motion planning and locomotion.

## Project Overview

The goal of this project is to simulate the behavior of the Spot robot in a Gazebo environment using ROS 2, enabling testing of basic movement, navigation, and control algorithms. The simulation is based on the **CHAMP quadruped control framework**, which allows for realistic walking behaviors and interactions with the environment.

## Features

* **ROS 2 Integration**: Fully integrated ROS 2 control system for Spot robot simulation.
* **Custom Gazebo World**: Realistic simulation environment with terrain and obstacles.
* **CHAMP Control Framework**: Gait and motion control for quadruped walking.
* **URDF/XACRO Model**: Custom Spot robot model for realistic simulation.
* **RViz Visualizations**: Integrated RViz for real-time visualization of robot status, navigation, and sensor data.
* **Basic Movement**: Demonstrated movement includes forward walking and direction control.

## Installation

1. Clone this repository:

   ```bash
   git clone https://github.com/yourusername/spot-ros2-gazebo-simulation.git
   cd spot-ros2-gazebo-simulation
   ```

2. Set up your ROS 2 workspace:

   ```bash
   mkdir -p ~/ros2_ws/src
   cd ~/ros2_ws/src
   git clone https://github.com/yourusername/spot-ros2-gazebo-simulation.git
   ```

3. Install the required dependencies:

   ```bash
   cd ~/ros2_ws
   rosdep install --from-paths src --ignore-src -r -y
   ```

4. Build the workspace:

   ```bash
   colcon build
   ```

5. Source the setup script:

   ```bash
   source ~/ros2_ws/install/setup.bash
   ```

## Launching the Simulation

To launch the Spot robot simulation in Gazebo, use the following command:

```bash
ros2 launch spot_bringup spot.gazebo.launch.py show_gui:=true verbose:=true
```

This will bring up the Spot robot in a Gazebo world with visualizations in RViz.

## Project Structure

```
spot-ros2-gazebo-simulation/
├── spot_bringup/
│   ├── launch/
│   ├── config/
│   └── ...
├── spot_gazebo/
│   ├── worlds/
│   ├── assets/
│   └── ...
├── spot_description/
│   ├── urdf/
│   └── ...
├── spot_navigation/
│   ├── launch/
│   ├── maps/
│   └── ...
└── README.md
```
## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

