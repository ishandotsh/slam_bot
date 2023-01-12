# SLAM and Navigation in Gazebo with ROS2

## Options

* in description/robot.urdf.xacro, choose either camera or depth_camera, not both.

## Launch Commands

Run rviz before gazebo because rviz sometimes doesn't show the /odom frame

```
    rviz2 -d ~/dev_ws/src/slam_bot/config/main.rviz
    ros2 launch slam_bot launch_sim.launch.py world:=~/dev_ws/src/slam_bot/worlds/obstacles.world
    
    # If use_ros2_control is set to true in slam_bot/launch/launch_sim.launch.py
    ros2 run teleop_twist_keyboard teleop_twist_keyboard --ros-args -r /cmd_vel:=/diff_cont/cmd_vel_unstamped
    # Otherwise
    ros2 run teleop_twist_keyboard teleop_twist_keyboard
```

