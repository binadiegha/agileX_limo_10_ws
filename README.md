# Autonomous Navigation with Path planning
This project is built on the AgileX LIMO robotic platform, running Ubuntu 18.04 and ROS Melodic. It focuses on core robotics functionalities, including environment mapping and localisation, leveraging both Gmapping and Karto-SLAM algorithms for SLAM (Simultaneous Localisation and Mapping). For autonomous navigation and path planning, the Dijkstra algorithm is implemented to determine the most efficient routes. To ensure seamless operation, the project requires Python 3, pip3, and a properly configured ROS Melodic environment. The integration of these tools allows for a robust and modular robotic system suitable for indoor navigation tasks.

## Setting up project
When you clone the repo. if it doesnt work. delete build and dev folders and rebuild the workspace.
Clonning this repo
``` bash
git clone https://github.com/binadiegha/agileX_limo_10_ws.git
``` 
Next, cd into the work space
``` bash 
cd agileX_limo_10_ws
```
ensure that the ports are accessible
```bash
ls /dev/ttyUSB*
```
this command should list the ports available. it could be ``` /dev/ttyUSB0 ``` or something similar depending on your device. ensure you note and select the correct port. If and access error shows up. run the command below to give write access:
```bash
sudo chmod -R 666 /dev/ttyUSB0
##replace USB0 with correct port number
```

## Installing dependencies
Ensure all ros necessary ROS Dependencies are running, if not, intall all ROS dependenceis 
``` bash
sudo apt update
sudo apt install ros-melodic-desktop-full
```

Next ensure Rviz, python serial and tf are installed on the machine

```bash
sudo apt install python3-pip python3-serial
sudo apt install ros-melodic-rviz # for Rviz 
sudo apt-get install ros-melodic-slam-karto # For KartoSLAM
sudo apt-get install ros-melodic-gmapping # For GMapping (optional)
sudo apt-get install ros-melodic-robot-pose-ekf # For odometry estimation
sudo apt-get install ros-melodic-usb-cam # For USB camera support
sudo apt-get install ros-melodic-tf # For coordinate frame transformation
```

#### Install more dependencies

## Running the project
First ensure that you are using the correct work space.
``` `bash 
  cd agileX_limo_10_ws
  source ~devel/setup.bash
```
to make this persistent, add the source to your bash file
```bash
echo "source ~/agileX_limo_10_ws/devel/setup.bash" >> ~/.bashrc
source ~/.bashrc
```
build the workspace:
```bash
catkin_make
```
Run the project
```bash
roslaunch limo_navigation navigation.launch
```

this command will open Rviz and run all all packages 

## Contributions
For Issues, please raise an issue in the issues page and for contributions, fork the project and make changes as you see fit. Cheers! 
