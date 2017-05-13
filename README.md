# Installation

##### 1. Install ROS' wstool and catkin tools:
Either
```
sudo apt install python-wstool
sudo apt install python-catkin-tools
```
or
```
sudo pip install -U wstool
sudo pip install -U catkin_tools
```

##### 2. Create and initialize ROS/Catkin workspace
Source your ROS installation
```
source /opt/ros/kinetic/setup.bash
```
create folder for workspace
```
mkdir gopigo_ws
cd gopigo_ws
```

Download the repository file containing all catkin packages and their location.

For GoPiGo only:
```
wget https://raw.githubusercontent.com/ros-gopigo/rosinstall-repo/master/ros-gopigo.rosinstall
```

For GoPiGo **with raspicam**:
```
wget https://raw.githubusercontent.com/ros-gopigo/rosinstall-repo/master/ros-gopigo-video.rosinstall
```
This will install the raspicam node and its dependencies that are not included in the ROS variant 'robot'.

You should now see the `ros-gopigo.rosinstall` or `ros-gopigo-video.rosinstall` file within your directory `gopigo_ws`.

##### 3. Download all packages in the workspace
```
wstool init src ros-gopigo.rosinstall
```
or
```
wstool init src ros-gopigo-video.rosinstall
```
respectively.

##### 4. Fetch remaining system dependencies
```
rosdep install --from-paths src --ignore-src --rosdistro kinetic -y -r --os=debian:jessie
```

##### 5. Build packages
```
catkin build
```

##### 6. Enable workspace and have fun
```
source devel/setup.bash
```
