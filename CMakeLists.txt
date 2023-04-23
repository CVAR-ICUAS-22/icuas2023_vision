cmake_minimum_required(VERSION 3.0.2)
project(icuas2023_vision)

set(PROJECT_DEPENDENCIES 
  rospy
  message_generation
  geometry_msgs
  cv_bridge
  sensor_msgs
)

find_package(catkin REQUIRED COMPONENTS
  ${PROJECT_DEPENDENCIES}
)

catkin_python_setup()
catkin_package()

catkin_install_python(PROGRAMS
  image_detections.py
  models.py
  DESTINATION ${CATKIN_PACKAGE_BIN_DESTINATION}
)

