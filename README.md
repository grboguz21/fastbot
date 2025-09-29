# FastBot ROS 2 Workspace

This repository contains the ROS 2 packages required to bring up and operate the **FastBot** robot.  
All core drivers are included so the robot can be tested on real hardware.

---

## 📦 Included Packages

The `fastbot` repository contains the following ROS 2 packages and more:

- **Motor Drivers**  
  Low-level motor control nodes and message definitions for wheel velocity and odometry.

- **Laser Drivers**  
  LSLiDAR ROS 2 driver for publishing laser scan data from the onboard LiDAR.

- **Camera Drivers**  
  Camera interfaces to publish image topics for perception tasks.

---

## 🔽 Download Instructions

1. Navigate to your ROS 2 workspace source folder:

    ```cd ~/ros2_ws/src```

2. Clone the FastBot repository:
    ```git clone https://github.com/<your-username>/fastbot.git```

3. Return to the root of your workspace:
    ```cd ~/ros2_ws```

4. Build the workspace:
    ```colcon build --symlink-install```

5. Source the setup file:
    ```source install/setup.bash```

---

## 🔽 Running the Robot Drivers 

To start all drivers (motors, lidar, and camera), launch the bringup file:
```ros2 launch fastbot_bringup fastbot_bringup.launch.py```

This will:
- Start the motor driver node
- Launch the LSLiDAR driver
- Bring up the camera driver

---

✅ Important Notes

- Make sure your FastBot is connected to the computer (via USB or network).
- Verify that the LiDAR and camera are properly powered.
- Use ros2 topic list to confirm all driver topics are being published.