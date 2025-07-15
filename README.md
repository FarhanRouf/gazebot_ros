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
STEP 4:
ros2 run teleop_twist_keyboard teleop_twist_keyboard cmd_vel:=/diff_cont/cmd_vel_unstamped

EXTRA:
You can also run rviz2 to see how ROS2 is seeing these topics and joint states.
ROS2 works with Gazebo through the ros_gz bridge, read gz_bridge.yaml under the src/config file.
