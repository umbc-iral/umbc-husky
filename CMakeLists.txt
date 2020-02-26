cmake_minimum_required(VERSION 2.8.3)
project(umbc_husky)

find_package(catkin REQUIRED COMPONENTS roslaunch)

catkin_package()
catkin_add_env_hooks(50.umbc_husky
  SHELLS sh DIRECTORY ${CMAKE_CURRENT_SOURCE_DIR}/env-hooks)

install(
  DIRECTORY meshes urdf launch
  DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}
)
