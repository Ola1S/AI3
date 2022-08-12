Installing the Arduino Robot Arm Package on ROS (noetic) Step by Step
Step 1 - Creating a ROS Package
To create Workspace run the following command consecutively:
mkdir -p ~/catkin_ws/src
cd ~/catkin_ws/
catkin_make
Step 2 - Add the Arduino Robot Arm Package to "src" Folder
In order to do this you have to run the commnds below in your terminal:
cd /catkin_ws/sre
sudo apt install git
git clone https://github.com/smart-methods/arduino robot arm
Step 3 - Install the Dependencies
run this instruction inside your workspace:
rosdep install --from-paths src --ignore-src -r -y
make sure you installed all these packages:
sudo apt-get install ros-noetic-moveit
sudo apt-get install ros-noetic-joint-state-publisher ros-noetic-joint-state-publisher-gui
sudo apt-get install ros-noetic-ros-controllers ros-noetic-ros-control
Step 4 - Configuring Arduino with ROS
First, Install Arduino IDE in Ubuntu from https://www.arduino.cc/en/software, then run the
following command after unzipping the folder:
sudo ./install.sh

Second, Launch the Arduino IDE

Third, Installing Binaries on the ROS workstation
You can install rosserial for Arduino by running:
sudo apt-get install ros-noetic-rosserial-arduino
sudo apt-get install ros-noetic-rosserial

5-Install ros_lib into the Arduino Environment
cd <sketchbook>/libraries
rm -rf ros_lib
rosrun rosserial_arduino make_libraries.py 
