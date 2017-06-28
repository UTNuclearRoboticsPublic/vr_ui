cmake_minimum_required(VERSION 2.8.3)
project(vr_ui)

find_package(catkin REQUIRED COMPONENTS geometry_msgs look_at_pose rospy std_msgs roscpp std_srvs)

catkin_package(CATKIN_DEPENDS roscpp INCLUDE_DIRS)

include_directories(${catkin_INCLUDE_DIRS})
link_directories(${catkin_LIBRARY_DIRS})

#############
## Install ##
#############

catkin_install_python(PROGRAMS nodes/test_rotate_cam
  DESTINATION ${CATKIN_PACKAGE_BIN_DESTINATION}
)
