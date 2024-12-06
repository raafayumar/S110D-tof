# S100D and S110D ToF Cameras - ROS Package

This repository contains the ROS package for S100D and S110D Time-of-Flight (ToF) cameras by Meere.

## Installation

### Prerequisites

- ROS Noetic
- Ubuntu 20.04

### Steps

1. Install ROS Noetic and Ubuntu 20.04.
2. Download the driver files from [this link](https://drive.google.com/file/d/1qhJkAUU_bpuT48fUx8X9OnJCEKcXi-vD/view) and move them into the 'src' folder of your ROS workspace.
3. Clone this repository into the 'src' folder of your ROS workspace.
4. Open a terminal in your ROS workspace folder and execute the following commands:
```bash
catkin_make
catkin_make clean
```
Once the commands are completed successfully, the ROS package for S100D or S110D should be installed.

## Usage

Follow the steps below to use the ROS package with the ToF camera:

1. Start the ros master by running the following command in a terminal:
```bash
roscore
```
2. Open a new terminal and navigate to your ROS workspace folder. Source the ROS setup.
3. Plug-in the camera to the PC and verify its connection by running:
```bash
lsusb
```
You should see the camera listed.

4. Launch the ToF camera driver and nodes using the following command:
```bash
roslaunch cubeeye_scube depth_camera.launch
```
5. Open another terminal, source the ROS setup, and run RViz:
```bash
rosrun rviz rviz
```
6. In RViz, add the relevant topics and visualize the camera data.

Make sure to adjust the commands and instructions based on your specific ROS workspace and setup.


## License

This project is licensed under the MIT License.
