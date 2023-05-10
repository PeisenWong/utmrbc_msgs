cmake_minimum_required(VERSION 2.8.3)
project(utmrbc_msgs)

find_package(catkin REQUIRED COMPONENTS roscpp roslaunch std_msgs std_srvs geometry_msgs sensor_msgs tf laser_geometry message_generation
)

add_message_files(
  FILES
  LED.msg
  AnalogInput.msg
  DigitalInput.msg
  BDC.msg
  HSPM.msg
  Ins.msg
  rns_nav.msg
  Odrive.msg
  VESC.msg
  PP.msg
  FB.msg
  feedback.msg
  PID.msg
) 

generate_messages(
  DEPENDENCIES std_msgs geometry_msgs
)

catkin_package(
  CATKIN_DEPENDS message_runtime
)

