# lslidar_decoder
## Overview
The data from Leishen Lidar N301 is read and then the data is used to convert the readings into point cloud and Publish it into node. The Lidar reflects the light from a laser source with the help of a rotating mirror and thec rays that reflect from the objects are read and a map is created.

In this code the data collected by the drivers is used and the decoding of the data takes place in order to generate a point-cloud of the map, later to be published on the node.
* It contains a C++ script "lslidar_n301_decoder.cpp" which uses the data provided by the driver to generate a point-cloud of the map.
* It also contains another "lslidar_n301_decoder_node.cpp" which publishes the decoded and converted data onto a ROS node.

## Software Requirements
1. Ubuntu 18.04
2. ROS Melodic

## Build and Complie

To create a new workspace faby_ws, open a terminal and run the following commands:

``` bash
mkdir -p ~/robot_ws/src
cd ~/robot_ws/src/
git clone https://github.com/maitreya98/lslidar_decoder.git
cd ..
catkin_make
source devel/setup.bash
```

## To launch and nodes execute:
```
cd ~/robot_ws
roslaunch lslidar_n301.launch
```

