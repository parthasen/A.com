# Capstone project @SDCND

![ros-graph](https://github.com/parthasen/autoeuvre/blob/master/imgs/final-project-ros-graph-v2.png)

#### Important Intel
1. Robot Operating System (ROS) that will first steer a virtual car in the simulator, and later on the code will be run on an actual car 'Carla'. 
2. ROS installed in Ubuntu, VM or Docker file
3. To really test your project on the simulator you will need a fast machine and probably a NVIDIA GPU for the traffic light recognition.
4. ROS and simulator connection is bit  flaky.
5. Simulator accepts only throttle or brake commands 


#### Steps

1. Clone the project repository `git clone https://github.com/udacity/carnd_capstone.git`
2. Need to install python dependencies 

        cd carnd_capstone
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
