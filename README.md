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

Download the repository file containing all catkin packages and their location:
```
wget https://raw.githubusercontent.com/ros-gopigo/rosinstall-repo/master/ros-gopigo.rosinstall
```

You should now see the `ros-gopigo.rosinstall` file within your directory `gopigo_ws`.

##### 3. Download all packages in the workspace
```
wstool init src ros-gopigo.rosinstall
```

##### 4. Build packages
```
catkin build
```

##### 5. Enable workspace and have fun
```
source devel/setup.bash
```
