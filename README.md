# 🤖 DD Bot – Differential Drive Robot

A simple Differential Drive Robot designed in Fusion 360 and brought into Gazebo using ROS 2 Jazzy.

## About the Project

I started this project to learn more about robot modelling and simulation using ROS 2.

First, I designed a Differential Drive Robot in Autodesk Fusion 360. After completing the design, I exported its components as STL files and used them to create a URDF/Xacro model.

Then I added the required launch files and configurations to my ROS 2 Python package and worked on getting the robot model into Gazebo Harmonic.

Finally, I was able to load and view my robot in Gazebo.

This project helped me understand how a robot designed in CAD software can be used in a robotics simulation.

## Tools Used

- Autodesk Fusion 360
- ROS 2 Jazzy Jalisco
- Gazebo Harmonic
- Python
- URDF / Xacro
- STL files
- Ubuntu Linux

## About the Robot

The robot is based on a differential drive design.

It includes:
- Base chassis
- Four wheel components
- LiDAR model

The mechanical parts were designed in Fusion 360 and then exported for use in the robot model.

## How I Made It

1. Designed the robot in Fusion 360.
2. Exported the individual parts as STL files.
3. Used those files in the URDF/Xacro model.
4. Added the required links and joints.
5. Configured the Gazebo-related files.
6. Created Python launch files for ROS 2.
7. Loaded the robot model into Gazebo Harmonic.

## Project Structure

```text
dd_robot_description/
│
├── config/
├── dd_robot_description/
├── launch/
│   ├── display.launch.py
│   └── gazebo.launch.py
│
├── meshes/
│   ├── base_link.stl
│   ├── lidar_1.stl
│   ├── wheel_1.stl
│   ├── wheel_2.stl
│   ├── wheel_3.stl
│   └── wheel_4.stl
│
├── resource/
├── test/
│
├── urdf/
│   ├── dd_robot.gazebo
│   ├── dd_robot.ros2control
│   ├── dd_robot.xacro
│   └── materials.xacro
│
├── worlds/
│   └── lidar_world.sdf
│
├── package.xml
├── setup.cfg
└── setup.py
```

## Requirements

- Ubuntu Linux
- ROS 2 Jazzy
- Gazebo Harmonic
- Python 3
- Colcon

## Build the Package

Open your terminal and go to your ROS 2 workspace:

```bash
cd ~/bot_ws
```

Build the package:

```bash
colcon build --packages-select dd_robot_description
```

Source the workspace:

```bash
source install/setup.bash
```

## Run the Robot

To open the robot in Gazebo:

```bash
ros2 launch dd_robot_description gazebo.launch.py
```

To view the robot in RViz2:

```bash
ros2 launch dd_robot_description display.launch.py
```

## Project Screenshot

### DD Bot in Gazebo Harmonic

<img width="1003" height="849" alt="image" src="https://github.com/user-attachments/assets/007a7413-20e6-451e-8e00-71843295e1db" />


## What I Learned

While working on this project, I got to learn and explore:

- Robot designing and assembly in Fusion 360.
- Exporting CAD parts as STL files.
- Converting a CAD model into URDF/Xacro.
- Working with links and joints.
- Creating a ROS 2 Python package.
- Writing launch files.
- Loading a robot model in Gazebo.

## What's Next?

There are still many things I would like to try with this robot:

- Making the robot move using differential drive control.
- Adding `/cmd_vel` control.
- Trying keyboard teleoperation.
- Adding a working LiDAR sensor.
- Exploring SLAM and Nav2.

## Author

**Ishan Borawle**
