# Making AUTOEUVRE.COM

![ros-graph](https://github.com/parthasen/autoeuvre/blob/master/imgs/final-project-ros-graph-v2.png)

https://github.com/parthasen/autoeuvre/edit/master/README.md

https://github.com/parthasen/autoeuvre/blob/note/ROS_VB.md

#### Important Intel
1. Robot Operating System (ROS) that will first steer a virtual car in the simulator, and later on the code will be run on an actual car 'Carla'. 
2. ROS installed in Ubuntu, VM or Docker file
3. To really test your project on the simulator you will need a fast machine and probably a NVIDIA GPU for the traffic light recognition.
4. ROS and simulator connection is bit  flaky.
5. Simulator accepts only throttle or brake commands 


#### Steps

1. Clone the project repository `git clone https://github.com/udacity/CarND-Capstone`
2. Need to install python dependencies 

        cd CarND-Capstone
        pip install -r requirements.txt
3. Make and run styx

        cd ros
        catkin_make
        source devel/setup.sh
        roslaunch launch/styx.launch
4. Run the simulator

        unzip lights_no_cars.zip
        cd lights_no_cars
        chmod +x ros_test.x86_64
        ./ros_test.x86_64
#### Nodes
##### Waypoint Node
        T1: roscore
        T2: cd CarND-Capstone/ros
            student@udacity:~/CarND-Capstone/ros$ roslaunch launch/styx.launch
        T3: rostopic list,rostopic info /final_waypoints,
        ** use source devel/setup.bash

##### DBW Node

        T4: student@udacity:~/CarND-Capstone/ros/src/twist_controller$

##### TLD Node

#### ROS
        T5: rosbag play -l <path_to_your.bag>
        T6: @udacity:~$ rviz
File > Open Config in RViz from Desktop...       


1. Testing:

        T1: roscore
        T2: student@udacity:~/CarND-Capstone/ros$ roslaunch launch/styx.launch
        T3: student@udacity:~/CarND-Capstone/ros$ rosmsg info styx_msgs/Lane

2. Real world testing

-- Download training bag that was recorded on the Udacity self-driving car (a bag demonstraing the correct predictions in autonomous mode can be found here) 
`https://drive.google.com/file/d/0B2_h37bMVw3iYkdJTlRSUlJIamM/view?usp=sharing` and `https://drive.google.com/open?id=0B2_h37bMVw3iT0ZEdlF4N01QbHc`
--Unzip the file `unzip traffic_light_bag_files.zip`
--Play the bag file `rosbag play -l traffic_light_bag_files/loop_with_traffic_light.bag`
--Launch your project in site mode 

                cd CarND-Capstone/ros
                roslaunch launch/site.launch
--Confirm that traffic light detection works on real life images

#### Dataspeed DBW
https://bitbucket.org/DataspeedInc/dbw_mkz_ros
