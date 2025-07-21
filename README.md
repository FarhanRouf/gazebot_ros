## Robot Package Template

This is a GitHub template. You can make your own copy by clicking the green "Use this template" button.

It is recommended that you keep the repo/package name the same, but if you do change it, ensure you do a "Find all" using your IDE (or the built-in GitHub IDE by hitting the `.` key) and rename all instances of `my_bot` to whatever your project's name is.

Note that each directory currently has at least one file in it to ensure that git tracks the files (and, consequently, that a fresh clone has direcctories present for CMake to find). These example files can be removed if required (and the directories can be removed if `CMakeLists.txt` is adjusted accordingly).



STEP 1:
colcon build --symlink-install

STEP 2:
source install/setup.bash

STEP 3:
ros2 launch gazebot_ros launch_sim.launch.py
Gazebo opens and you can use the teleop on Gazebo or do the next step to control it from terminal

To visualize the lidar, search Visualize Lidar and click the refresh so it autoselects scan.
In RViz, add laserscan and choose the scan topic.

LIDAR DEMO:
<img width="1002" height="657" alt="GZ_Lidar" src="https://github.com/user-attachments/assets/61026719-2055-4c73-b0f5-20ee1d3ff83c" />
<img width="621" height="435" alt="RVIZ_Lidar" src="https://github.com/user-attachments/assets/cc5d60a8-a3bb-416f-a6cc-25eb00518398" />


STEP 4:
ros2 run teleop_twist_keyboard teleop_twist_keyboard cmd_vel:=/diff_cont/cmd_vel_unstamped

https://github.com/user-attachments/assets/a667c44e-1943-4ac9-a5e3-28f7da8179be

EXTRA:
You can also run rviz2 to see how ROS2 is seeing these topics and joint states.
ROS2 works with Gazebo through the ros_gz bridge, read gz_bridge.yaml under the src/config file.
