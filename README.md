# SLAM and Navigation in Gazebo with ROS2

### Launch Commands

Run rviz before gazebo else rviz doesn't show the /odom frame

```
    rviz2 -d ~/dev_ws/src/slam_bot/config/move_bot.rviz
    ros2 launch slam_bot launch_sim.launch.py world:=~/dev_ws/src/slam_bot/worlds/obstacles.world
    ros2 run teleop_twist_keyboard teleop_twist_keyboard
```