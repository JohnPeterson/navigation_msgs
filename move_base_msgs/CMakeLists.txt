cmake_minimum_required(VERSION 2.8.3)
project(move_base_msgs)

find_package(catkin REQUIRED
  COMPONENTS
    message_generation
    nav_msgs
    actionlib_msgs
    geometry_msgs
)

add_action_files(
  DIRECTORY
    action
  FILES
    MoveBase.action
)

generate_messages(
  DEPENDENCIES
    nav_msgs
    actionlib_msgs
    geometry_msgs
)

catkin_package(
)
