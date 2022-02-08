cmake_minimum_required(VERSION 2.8.3)
project(autoware_msgs)

find_package(catkin REQUIRED COMPONENTS
  message_generation
  geometry_msgs
  std_msgs
)

add_message_files(
  DIRECTORY msg
  FILES
    AccelCmd.msg
    BrakeCmd.msg
    ControlCommand.msg
    Gear.msg
    LampCmd.msg
    SteerCmd.msg
    VehicleCmd.msg
)

generate_messages(
  DEPENDENCIES
    geometry_msgs
    std_msgs
)

catkin_package(
  CATKIN_DEPENDS
    message_runtime
    geometry_msgs
    std_msgs
)
