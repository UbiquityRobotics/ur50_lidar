cmake_minimum_required(VERSION 2.8.3)
project(ur50_lidar_msgs)

find_package(catkin REQUIRED COMPONENTS
  message_generation
  std_msgs
)

add_message_files(
  DIRECTORY msg
  FILES
  LslidarN301Packet.msg
  LslidarN301Point.msg
  LslidarN301Scan.msg
  LslidarN301Sweep.msg
  LslidarN301Difop.msg
)
generate_messages(DEPENDENCIES std_msgs)

catkin_package(
  CATKIN_DEPENDS message_runtime std_msgs
)
