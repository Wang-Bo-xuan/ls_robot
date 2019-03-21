cmake_minimum_required(VERSION 2.8.3)
project(ls_robot_teleop)

find_package(catkin REQUIRED COMPONENTS
            roscpp
            geometry_msgs)

include_directories(${catkin_INCLUDE_DIRS})

catkin_package(
  INCLUDE_DIRS
  CATKIN_DEPENDS roscpp geometry_msgs
  DEPENDS
)

add_executable(ls_robot_keyboard_teleop src/keyboard_teleop.cpp)
target_link_libraries(ls_robot_keyboard_teleop ${catkin_LIBRARIES})
