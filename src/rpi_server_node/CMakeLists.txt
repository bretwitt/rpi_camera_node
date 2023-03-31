cmake_minimum_required(VERSION 3.0.2)
project(rpi_server_node)

find_package(catkin REQUIRED)

catkin_package(
	INCLUDE_DIRS scripts
	LIBRARIES ${PROJECT_NAME}
	CATKIN_DEPENDS rospy
)



catkin_install_python(PROGRAMS scripts/server.py
  DESTINATION ${CATKIN_PACKAGE_BIN_DESTINATION}
)
