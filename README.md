behaviourdetection
=====

This repository contains the source code for the ROS workspace including the NTNU Cyborg's Computer Vision Module, which should be installed on the Jetson TX1 developer board. The system uses the ZED camera to detect human behaviour.

Node name: jetsontx1_cvmodule Language: Python
### Dependencies
Following packages and ther dependendencies should be installed, before proceeding to the "Installation" section:
1. [OpenCV](https://pypi.org/project/opencv-python/) (Allready installed if TX1 is flashed with JetPack)
0. [CUDA](https://developer.nvidia.com/cuda-downloads) (Allready installed if TX1 is flashed with JetPack)
0. Python 2.7 (Allready installed if TX1 is flashed with JetPack)
0. [ZED SDK](https://www.stereolabs.com/docs/installation/jetson/)
0. [ZED Python API](https://github.com/stereolabs/zed-python-api)
### Installation
1. Install and configure a catkin ROS environment by following [the ROS tutorials](http://wiki.ros.org/ROS/Tutorials)
0. Clone this repository and copy the folder "jetsontx1_cvmodule" into the src folder in your ROS workspace where the ROS packages should be located.
0. Build the ROS package by using the command "catkin_make" in the catkin workspace terminal window.
0. Locate the pyyolo folder in the terminal and install using the commands as following:
    1. make
    0. rm -rf build/
    0. python setup_gpu.py build
    0. sudo python setup_gpu.py install

**Note:** This

### Run the system
To launch the main code publishing info about detected human behaviour:
´´´
rosrun jetsontx1_cvmodule behaviourdetection.py
´´´
