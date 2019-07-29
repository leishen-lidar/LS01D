cmake_minimum_required(VERSION 2.8.3)
project(talker)

find_package(catkin REQUIRED COMPONENTS
  roscpp
  rospy
  std_msgs
  sensor_msgs
)


catkin_package()

include_directories(
  ${catkin_INCLUDE_DIRS}/src
)

add_executable(talker src/main.cpp src/uart_driver.cpp)
target_link_libraries(talker ${catkin_LIBRARIES})

