# RI_Part3
This Repository contains only Part 1 of the project.

1. urdf_quad contain the details about the robot Quad (only one leg).
2. moveit3 is generated with moveit.
3. project_control consist of node to control the robot.

##Installation
The package need to be instal in your catkin workspace.
```
cd catkin_ws/src
git clone https://github.com/Seekcha/RI_Part3.git
catkin build
cd ..
source devel/setup.bash
```

## Execution
### Front left leg in RVIZ
Open front left leg in RVIZ in first terminal:
```
source devel/setup.bash
roslaunch moveit3 demo.launch
```

#### Movement
Launch direct.launch in second terminal:
```
source devel/setup.bash
roslaunch project_control direct.launch
```
#### Calling function
Launch in third terminal:
source devel/setup.bash
rosservice call /direct_kin_service_front_left_leg "
joint1:
 data: 1.2100
joint2:
 data: 0.000
joint3:
 data: 0.1700
joint4:
 data: -1.629
 "
