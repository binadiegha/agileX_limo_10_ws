# Autonomous Navigation with Path planning
This project uses the AgileX limo running ubuntu 18 and ROS melodic. It covers mapping and localisation using Gmapping and Karto-SLAM algorithms and for path planning, Dijkstra is utilised.
This project requires Python3, Pip3 and ROS-Melodic to run smoothly.

When you clone the repo. if it doesnt work. delete build and dev folders and rebuild the workspace.
Clonning this repo
``` bash
git clone https://github.com/binadiegha/agileX_limo_10_ws.git
``` 
Next, CD into the work space
``` bash 
cd agileX_limo_10_ws
```
Ensure all ros necessary ROS Dependencies are running, if not, intall all ROS dependenceis 
``` bash
sudo apt update
sudo apt install ros-melodic-desktop-full
```

