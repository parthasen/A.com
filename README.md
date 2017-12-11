# Capstone project @SDCND

![ros-graph](https://github.com/parthasen/autoeuvre/blob/master/imgs/final-project-ros-graph-v2.png)

#### Steps

    Clone the project repository

git clone https://github.com/udacity/carnd_capstone.git

    Install python dependencies

cd carnd_capstone
pip install -r requirements.txt

    Make and run styx

cd ros
catkin_make
source devel/setup.sh
roslaunch launch/styx.launch

    Run the simulator

unzip lights_no_cars.zip
cd lights_no_cars
chmod +x ros_test.x86_64
./ros_test.x86_64
