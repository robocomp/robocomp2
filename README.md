# robocomp2
New Robocomp 2.0 framwork

```shell
apt update
apt install python3 python3-pip cmake vim git wget -y
pip3 install vcstool colcon-common-extensions
mkdir -p ~/robocomp_ws/src
cd ~/robocomp_ws
wget https://raw.githubusercontent.com/robocomp/robocomp2/main/robocomp.repos
# robocomp dependencies
apt install qtbase5-dev libqt5xmlpatterns5-dev libopenscenegraph-dev libgsl-dev
vcs import src < robocomp.repos
colcon --log-level 5 build 
```

# TODO
* ROS have plenty of tools we could use: colcon, rosdep
* Check how to create a ros2 package for one of the robocomp libraries
  * Trying with dsr:
    * https://github.com/orensbruli/ros_dsr
    * cppitertools created as vendor package
    * qmat
      * Moving CMakeLists.txt to ament cmake
        * ament_cmake documentation https://docs.ros.org/en/humble/How-To-Guides/Ament-CMake-Documentation.html
  * ROS 2 python package https://roboticsbackend.com/create-a-ros2-python-package/
  * ROS1 vs ROS 2 diffs https://roboticsbackend.com/ros1-vs-ros2-practical-overview/
  * 