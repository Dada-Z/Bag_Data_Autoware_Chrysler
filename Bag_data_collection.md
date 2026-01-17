# Bag data collection

Tasks:
The following road segments corresponding to Seg1 to Seg10

Field test:

- See 'Field_Test.png' 

The .bag data example (`r1-s5-2025-11-18-09-01-03-clear`):

- sample name: `sample_17_27s.bag`

| **Topic**                | **Description**             |
| ------------------------ | --------------------------- |
| `/camera_fl/image_raw`   | Front-left camera (raw RGB), similar to `camera_fl/image_raw` |
| `/camera_fr/camera_info` | Camera intrinsic params     |
| `/points_raw`            | 3D point cloud data         |
| `/velodyne_packets`      | Raw Velodyne packet stream  |
| `/gps/imu`               | IMU data (sensor_msgs/Imu) — raw IMU |
| `/vehicle/joint_states`  | Joint angles, positions, velocities  |
| `/novatel/oem7/bestvel`       | GPS-estimated velocity             |
| `/vehicle/wheel_speed_report` | Individual wheel speeds            |
| `/vehicle/joint_states`       | Can include wheel rotation rates [^1] |
| `/vehicle/steering_report`    | Actual measured steering angle     |

Update in January 2026:

- A new bag data was collected in January, 2026 on Vine St, Lincoln, NE. See `2026-01-07-vine-wb-GPS-map.pdf` file.

[^1]: It contains ['wheel_fl', 'wheel_fr', 'wheel_rl', 'wheel_rr', 'steer_fl', 'steer_fr']. Position and velocity are included and be used to estimate vehicle speed.
