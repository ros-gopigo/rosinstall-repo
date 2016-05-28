# Installation

##### 1. Install ROS' wstool
Either
```
sudo apt-get install python-wstool
```
or
```
sudo pip install -U wstool
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

Download the repository file containing all catkin packages and their location. You need to select the link appropriate for your ros version:

For ROS `jade`:
```
wget https://raw.githubusercontent.com/ros-gopigo/rosinstall-repo/jade/ros-gopigo.rosinstall
```
For ROS `kinetic`:
```
wget https://raw.githubusercontent.com/ros-gopigo/rosinstall-repo/kinetic/ros-gopigo.rosinstall
```

You should now see the `ros-gopigo.rosinstall` file within your directory `gopigo_ws`.

##### 3. Download all packages in the workspace
```
wstool init src ros-gopigo.rosinstall
```

##### 4. Build packages
```
catkin_make
```

##### 5. Enable workspace and have fun
```
source devel/setup.bash
```
