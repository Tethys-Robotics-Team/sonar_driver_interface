cmake_minimum_required(VERSION 3.5)
project(sonar_driver_interface)


find_package(catkin REQUIRED COMPONENTS
  rospy
  std_msgs
  message_generation
)

add_message_files(
  FILES
  SonarBearings.msg
  SonarConfiguration.msg
  SonarConfigurationChange.msg
)

generate_messages(
  DEPENDENCIES
  std_msgs
)

catkin_package(
  CATKIN_DEPENDS message_runtime
)

include_directories(  
  ${catkin_INCLUDE_DIRS} 
)
