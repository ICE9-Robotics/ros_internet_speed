cmake_minimum_required(VERSION 3.0.2)
project(ros_internet_speed)

find_package(catkin REQUIRED COMPONENTS
  message_generation
  rospy
  std_srvs
  std_msgs
)

# catkin_python_setup()

################################################
## Declare ROS messages, services and actions ##
################################################
add_message_files(
  FILES
  InternetSpeedReport.msg
)

generate_messages(
  DEPENDENCIES
  std_msgs
)

###################################
## catkin specific configuration ##
###################################
catkin_package(
    LIBRARIES ${PROJECT_NAME}
    CATKIN_DEPENDS rospy std_srvs std_msgs message_generation message_runtime
)

#############
## Install ##
#############
catkin_install_python(
  PROGRAMS node/internet_speed_node
  DESTINATION ${CATKIN_PACKAGE_BIN_DESTINATION}
)