# MORPH : Modular Open Robotics Platform for Hackers
An affordable modular platform for open robotics development for hackers. Provides a jump start to build your own robot.
For further documentation see <https://hackaday.io/project/25730-morph-modular-open-robotics-platform-for-hackers>

## Introduction
This is the main repository for the morph stack. All packages for the morph stack have their own repository but are linked as submodules
from this main repository. 

## Installation
### ROS distribution
The morph stack has been tested with the ROS Indigo and Kinetic distributions. For instructions on installing ROS see the [ROS wiki](http://wiki.ros.org/).

### ROS package dependencies
The morph stack uses the Turtlebot stack and ros_control. Follow [installation instructions for the Turtlebot stack](http://wiki.ros.org/turtlebot/Tutorials/indigo/Turtlebot%20Installation).
Other dependencies are linked as submodule from the morph repository.
```
sudo apt-get install ros-indigo-ros-control ros-indigo-ros-controllers
```

### Create a catkin_workspace
```
mkdir -p ~/morph_ws/src
cd ~/morph_ws
catkin_make
```

### Checkout and initialize and update submodules
```
cd ~/morph_ws/src
git clone https://github.com/roaldlemmens/morph.git
cd morph
git submodule init
git submodule update
```
### Compile code
```
cd ~/morph_ws
catkin_make
```
If your environment is setup correctly, you shouldn't have any compilation errors. If so you are probably missing dependencies.
