# Capstone project @SDCND

![ros-graph](https://github.com/parthasen/autoeuvre/blob/master/imgs/final-project-ros-graph-v2.png)

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
