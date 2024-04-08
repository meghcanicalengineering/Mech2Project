# Project Hardware/Software
**Hardware**
- A1M8 Slamtec LiDAR
- Raspberry Pi 4 Model B

**Software**
- Ubuntu 22.04 Jammy Jellyfish
- ROS2 Humble Hawksbill
- Rviz2
- Gazebo(?)
- slam_toolbox
- rplidar

# Viewing LiDAR PointCloud in RViz
1. Start the Pi, change time and date
2. Open the terminal
3. Change directory to ros2 workspace  
    ```cd ~/ros2_ws/```
4. Run bash source for starting ROS Humble  
    ```source /opt/ros/humble/setup.bash```
5. Run bash source for package environment setup  
   ```source ./install/setup.bash```
6. Change directory to RPLiDAR source file  
    ```cd src/rplidar_ros/```
7. Run sh source for udev rules  
   ```source scripts/create_udev_rules.sh```
8. Run RPLiDAR node and view in RViz (this is from a single command)  
    ```ros2 launch rplidar_ros view_rplidar_a1_launch.py```

From here, the node will open and RViz will open, showing the PointCloud from the LiDAR data  
Change delay to allow for changes in points to build for some time  
Change size of points to visualize better
