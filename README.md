# robot

# Download and install VirtualBox and VirtualBox Extension Pack
https://www.virtualbox.org/wiki/Downloads

# Download ros indigo64bit VM
http://nootrix.com/downloads/

# Configure and start VM


# Add sources for ros packages
sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu trusty main" > /etc/apt/sources.list.d/ros-latest.list'
wget https://raw.githubusercontent.com/ros/rosdistro/master/ros.key -O - | sudo apt-key add -
sudo apt-get update

# Install UR ros driver
http://wiki.ros.org/universal_robot

# Install MoveIt!
http://moveit.ros.org/install/

# as always start roscore
roscore

# start simulated robot node
rosrun turtlesim turtlesim_node

# start keyboard input driver node
rosrun turtlesim turtle
