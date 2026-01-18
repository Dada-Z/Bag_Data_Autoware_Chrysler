# Bag data analysis

## Review bag data
The following steps showing how to review bag data in ROS:

- Open a Terminal: `roscore`
- Open another Terminal: `rosbag info NAME.bag`
++ Check time, duration, and topics

Visualize bag data in RViz:

- `roscore`
- `rosbag play -l NAME.bag`
- `rviz`

## Extract a sample from bag 
Using the following command to obtain a sample for 10 seconds:
- `rosbag filter NAME.bag short_sample_5_15s.bag \ '5.0 < t.to_sec() < 15.0'`
++ If the time is not this format, try this. `"1763478080.863850 < t.to_sec() < 1763478090.863919"`

## Extract images 
Install open-cv as first.
- `sudo apt install ros-noetic-cv-bridge python3-opencv`
- `sudo apt install ros-noetic-cv-bridge`

Create a work space and package
- ``
