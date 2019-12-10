
ssh into the odroid
run command: screen
to start plane run: roslaunch testDec03.launch

on computer set ROS settings to connect to the plane (set ROS MASTER URI

RC override means: switch is flipped, or a stick is deflected, or that the autopilot is commanding a throttle value higher than you are)

Useful ROS topics:
status - indicates if it's armed and in RC override
rcraw - shows values being received from controller
output_raw - what is being commanded to the motors (takes into account rc override)
command - slightly higher level of control (does not take into account rc override)

docs.rosflight.org go to param config page, and can learn how to set them
rc attitude override
rc throttle override

get plane into the air and have safety pilot set the trims where they feel comfortable
calibrate rc trims - this sets those trim values as the base values for steady flight

