cmake_minimum_required(VERSION 2.8.3)
project(rr_control_input_manager)

## Find catkin macros and libraries
## if COMPONENTS list like find_package(catkin REQUIRED COMPONENTS xyz)
## is used, also find other catkin packages
find_package(catkin REQUIRED COMPONENTS)

catkin_package()

install(DIRECTORY
  launch/
  DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}/launch
)

catkin_install_python(PROGRAMS
  scripts/control_input_manager.py
  scripts/xbox_mapper.py
  DESTINATION ${CATKIN_PACKAGE_BIN_DESTINATION}
)
