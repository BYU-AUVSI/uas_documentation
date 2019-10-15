# Appendix A: Quick Start Guide

The simplest system to use for code development is arguably Linux. Because compiling from source is so much simpler on Ubuntu, for example, than on Windows, that is our operating system of choice. Another advantage of Linux is that it is incredibly customizable. However, this can also complicate your install of ROS if you have made major changes to system defaults, terminal command aliases, or your PATH. You should be able to work through any error messages you encounter, but if not, a fresh install of Ubuntu should do the trick.

The latest LTS (Long Term Support) release of ROS is ROS Melodic. The only release of Ubuntu that is supported by ROS Melodic is Ubuntu Bionic (18.04). The Ubuntu operating system is free to download and use and each LTS release is guaranteed five years of free security and maintenance updates by Canonical, the company supporting its development.

The best way to run and use the existing code is by installing it on your own machine. We _strongly_ recommended that you run Ubuntu as a dual boot rather than using virtual machine (there is an excellent tutorial [here](https://www.tecmint.com/install-ubuntu-alongside-with-windows-dual-boot) and [here](https://howtoubuntu.org/how-to-install-ubuntu-18-04-bionic-beaver)). Virtual machines can have unexplainable issues connecting to the networking hardware and peripheral devices of the host operating system. It is better to partition your hard drive and install Ubuntu in the first place than to need to switch over later and reconfigure your whole machine. Ubuntu requires at a minimum 20 GB of free space (significantly less than Windows), but 40-50 GB is recommended.

## Configuring Your Machine
These are the necessary steps for getting your computer ready to run the AUVSI software.
* Install Ubuntu 18.04 as a dual-boot system along with your other operating system(s). I _highly_ recommend dual booting rather than trying to use a Virtual Machine. I used a VM for the first few months of AUVSI but I started running into weird network and device issues, so I had to switch over to a dual boot system and essentially start over. I have a bootable USB with 18.04 on it, anyone who wants to use it is welcome to get it from me in the MAGICC lab. See https://howtoubuntu.org/how-to-install-ubuntu-18-04-bionic-beaver for more instructions. *Note: Don't install any version besides 18.04 - ROS Melodic only officially supports 18.04 and all of the MAGICC lab code you'll be using is meant to run on Melodic.*
* On your Ubuntu 18.04 installation:
* Install ROS Melodic (http://wiki.ros.org/melodic/Installation/Ubuntu)
* Install git (`sudo apt install git`)
* Install python3, either by using the following, or by installing Anaconda (which can make switching between Python2 and Python3 easier)
```
sudo apt install python3 python3-pip
pip3 install numpy matplotlib 
```
* I would also recommend that you get a github.com account and be added to the byu-auvsi organization (github.com/byu-auvsi)

## Creating your workspace
All of the autopilot code that is used for AUVSI uses ROS. ROS provides a great set of tools and a system for allowing multiple "nodes" to communicate with each other, regardless of the computer that they are on as long as the computers are networked with each other.

Here's the steps to get a simulation environment up and running:
1. Set up a ROS catkin workspace
```
mkdir -p auvsi_ws/src
cd auvsi_ws
catkin_make
cd src
```

2. Clone the AUVSI repositories into `src`
There's a bunch of these and honestly this process could probably be automated somehow.
```
# Essential
git clone https://github.com/BYU-AUVSI/uav_msgs.git
git clone https://github.com/inertialsense/inertial_sense_ros.git
git clone https://github.com/byu-magicc/rosflight_plugins.git
git clone https://github.com/BYU-AUVSI/rosflight.git
git clone https://github.com/BYU-AUVSI/rosplane.git

# Fun to watch
git clone https://github.com/BYU-AUVSI/ros_groundstation.git

# Useful for more than just flying
git clone https://github.com/BYU-AUVSI/interop_pkg.git
git clone https://github.com/rosflight/rosflight_joy.git

# Broken, probably shouldn't install
git clone https://github.com/BYU-AUVSI/metis.git
```

*Note:* you may also need to install eigen-stl-containers
`sudo apt install ros-melodic-eigen-stl-containers`


3. Make the workspace and source the `setup.bash`
```
cd ../
catkin_make
source devel/setup.bash
```

<!--4. Run metis
```
roslaunch metis fake_interop.launch
```
-->
