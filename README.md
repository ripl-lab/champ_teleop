# champ_teleop
Champ Quadruped Robot's teleoperation node. This is a forked version of [teleop_twist_keyboard](https://github.com/ros-teleop/teleop_twist_keyboard/blob/master/teleop_twist_keyboard.py). 

The software has been modified to control the robot's whole-body pose (roll, pitch, yaw).

## How to use
### Using keyboard:

    ros2 launch b2_mujoco b2_mujoco_champ.launch.py

### Using controller:

Terminal 1:

    ros2 run joy joy_node

If not install:

    sudo apt install ros-humble-joy

Terminal 2:

    ros2 launch b2_mujoco b2_mujoco_champ.launch.py

## Controlling the robot with Joystick

Left Joystick:
- Left stick up / down - Walk forward / backward
- Left stick left / right - Turn on the spot
- LB (hold) + left stick left / right - Strafe sideways instead of turning

Right Joystick:
- Right stick left / right - Tilt the body side to side (roll)
- RB (hold) + right stick left / right - Twist the body (yaw) instead of rolling
- Right stick up / down - Tilt the body forward / back (pitch)
- RT (squeeze) - Lower the body
