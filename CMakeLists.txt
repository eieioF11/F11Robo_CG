cmake_minimum_required(VERSION 3.0.2)
project(F11Robo_CG)

find_package(catkin REQUIRED COMPONENTS
  actionlib
  move_base_msgs
  roscpp
  std_msgs
)

catkin_package(
  #INCLUDE_DIRS include
  LIBRARIES F11Robo_CG
  CATKIN_DEPENDS actionlib move_base_msgs roscpp std_msgs
  DEPENDS system_lib
)

add_executable(goal_generator src/simple_goal_generator.cpp)

target_link_libraries(goal_generator
  ${catkin_LIBRARIES}
)

include_directories(
# include
  ${catkin_INCLUDE_DIRS}
)

