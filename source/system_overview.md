# System Overview

The Unmanned Aerial System used by the Brigham Young University (BYU) competition team is based on the the book written by the sponsor of the team, Dr. Tim McLain (Beard, R. and McLain T. Small Unmanned Aircraft: Theory and Practice, Princeton University Press, Princeton, NJ, 2012.). As such, it uses many of the technologies originally pioneered in the BYU MAGICC (Multiple AGent Intelligent Coordination and Control) Lab, of which Dr. McLain is a founder.

The main framework underpinning the entire system is the Robot Operating System (ROS). A fully open-source package that was first conceived at Stanford University, ROS has grown such that its ecosystem is now used by tens of thousands of users throughout the world. Since it is licensed under the permissive BSD license (the abbreviation "BSD" originates from the license for the Berkeley Software Distribution, a Unix-like operating system. As its been changed and revised, its descendants are referred to as modified BSD licenses), users of the framework maintain full ownership, control, and rights to their code. There is no requirement that the source code be distributed or that a fee be paid for the use of ROS.

The MAGICC Lab has extended the capabilities of ROS with the creation of the ROSflight package. It provides an interface between ROS and any platform running the ROSflight firmware. Additionally, another package created in the MAGICC Lab, ROSplane, implements a limited-feature autopilot that can be used to fly the actual flight platform or its simulation equivalent using Gazebo, another open-source software. In theory, these packages are complete and shouldn't require modification by competition team members. Of course, bugs may be found and fixes implemented, but for the most part, these packages may be treated as black boxes that perform their functions correctly.
