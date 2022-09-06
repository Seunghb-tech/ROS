cmake_minimum_required(VERSION 3.0.2)
project(my_custom_srv_msg_pkg)

find_package(catkin REQUIRED COMPONENTS
  std_msgs
  message_generation
)

add_service_files(
  FILES
  MyCustomServiceMessage.srv
)

generate_messages(
  DEPENDENCIES
  std_msgs
)

catkin_package(
  CATKIN_DEPENDS rospy
)

include_directories(
  ${catkin_INCLUDE_DIRS}
)
