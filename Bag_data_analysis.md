# Bag data analysis

## Review bag data
The following steps showing how to review bag data in ROS:

- Open a Terminal: `rosbag info NAME.bag`

++ Check time, duration, and topics

Visualize bag data in RViz:
- `roscore`
- `rosbag play -l NAME.bag`
- `rviz`

## Extract a sample from bag 
Using the following command to obtain a sample for 10 seconds:
- `rosbag filter NAME.bag short_sample_5_15s.bag \ '5.0 < t.to_sec() < 15.0'`

If the time is not this format, try this. 
- `"1763478080.863850 < t.to_sec() < 1763478090.863919"`

## Extract images 
### Install open-cv tool first.
- `sudo apt install ros-noetic-cv-bridge python3-opencv`
- `sudo apt install ros-noetic-cv-bridge`

### Create a work space:
- `mkdir catkin_ws`
- `cd catkin_ws`
- `mkdir src`
- `catkin init`
- `catkin build`

### Create a package
- `cd ~/catkin_ws/src/`
- `catkin_create_pkg my_camera_tools std_msgs rospy sensor_msgs cv_bridge image_transport`

Move the python file to `catkin_ws/src/my_camera_tools/script` then
- `chmod +x ~/catkin_ws/src/my_camera_tools/scripts/extract_image.py`
- `catkin_make`

### Extract images from bag data
- `roscore`
- CTRL + SHIFT + T `source devel/setup.bash`
- `rosrun my_camera_tools extract_image.py [bag file]`
- CTRL + SHIFT + T `rosbag play [bag file]`

## Extract a video
Check frames per second (FPS) first. 
- `rostopic hz /camera_fl/image_raw` 

The relationship of number of images, duration, and FPS is shown below.
- If the total duration is 70 seconds and there are 338 images are generated. Then,
- FPS = 339/70 = 4.8. This should match the output of [^1]

Play bag data and run the following code to obtain a video.
- `ffmpeg -framerate 4.8 -i %*.jpg -c:v libx264 -pix_fmt yuv420p out_video.mp4` [^2]


[^1]: The output of `rostopic hz /camera_fl/image_raw`.
[^2]: yuv420p is not a resolution. 


