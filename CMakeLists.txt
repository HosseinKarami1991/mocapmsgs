cmake_minimum_required(VERSION 2.8.3)
project(mocap_msgs)


find_package(catkin REQUIRED COMPONENTS
  mocap
  message_generation
roscpp
std_msgs
)


add_message_files(
   DIRECTORY msg
   FILES
   mocapvector.msg

 )


generate_messages(
   DEPENDENCIES
   mocap
   geometry_msgs
   std_msgs 
 )


catkin_package(
#  INCLUDE_DIRS include
#  LIBRARIES mocap_msgs
  CATKIN_DEPENDS mocap message_generation  geometry_msgs std_msgs 
)
include_directories(
  ${catkin_INCLUDE_DIRS}
)


