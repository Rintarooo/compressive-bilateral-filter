cmake_minimum_required(VERSION 3.0.2)
project(jointbilateralfilter)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++14 -Wall")# -g3
find_package(OpenCV REQUIRED)

### directories where header files exists
include_directories(
  ${OpenCV_INCLUDE_DIRS}
  include/
)

add_executable(main
  main.cpp
)

target_link_libraries(main
  ${OpenCV_LIBRARIES}
)

# for debug
message(WARNING "prefix ${CMAKE_PREFIX_PATH}")    

message("-- OpenCV --")
message(WARNING "version ${OpenCV_VERSION}")
message(WARNING "install path ${OpenCV_INSTALL_PATH}") 
message(WARNING "config path ${OpenCV_CONFIG_PATH}") # look at the output of this message
message(WARNING "libs ${OpenCV_LIBS}")
message(WARNING "include dirs ${OpenCV_INCLUDE_DIRS}")