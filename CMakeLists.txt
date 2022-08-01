cmake_minimum_required(VERSION 3.1.3)
project(abb_irb4600_moveit_plugins)

find_package(catkin REQUIRED COMPONENTS
  moveit_core
  pluginlib
  roscpp
  tf2_kdl
  tf2_eigen
)
moveit_build_options()

include_directories(${catkin_INCLUDE_DIRS})

find_package(LAPACK REQUIRED)

catkin_package(
  LIBRARIES
  CATKIN_DEPENDS
    moveit_core
    pluginlib
    roscpp
)

add_subdirectory(abb_irb4600_40_255_kinematics)
