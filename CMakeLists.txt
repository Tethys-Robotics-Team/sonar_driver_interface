cmake_minimum_required(VERSION 3.5)
project(sonar_driver_interfaces)


find_package(catkin REQUIRED COMPONENTS
        message_generation
        std_msgs
        )

add_message_files(
        DIRECTORY msg
        FILES
        SonarConfiguration.msg
        SonarConfigurationChange.msg
)

generate_messages(
        DEPENDENCIES
        std_msgs
)

catkin_package(
        CATKIN_DEPENDS message_runtime std_msgs
)

include_directories(  ${catkin_INCLUDE_DIRS} )