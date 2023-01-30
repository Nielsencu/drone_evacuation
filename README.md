# Setup
MAVROS Installation (generates the .rosinstall in this repo)
https://docs.px4.io/main/en/ros/mavros_installation.html
Git clone the remaining folders in the repository.

Install ROS packages
- Slam Toolbox
- Robot localization

## How to run
Start up lidar node, laser scan matcher, slam_toolbox, move_base.
`roslaunch offboard_py lidar.launch`
Converts mavlink messages to ROS topics.
`roslaunch mavros px4.launch`
Maps mavros imu topic to /imu/data for laser scan matcher.
`rosrun topic_tools relay /mavros/imu/data /imu/data`

Launching Simulation
`cd ~/PX4-Autopilot && make px4_sitl gazebo`