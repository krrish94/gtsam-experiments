cmake_minimum_required(VERSION 2.6)

project(helloWorld)

set(GTSAM_DIR "/home/km/libs/gtsam-3.2.1/build")
find_package(GTSAM REQUIRED)
include_directories(${GTSAM_INCLUDE_DIR})
include_directories(${GTSAM_DIR})
include_directories("${GTSAM_DIR}/build")
link_directories(${GTSAM_LIBRARY_DIRS})

add_executable(helloWorld helloWorld.cpp)
target_link_libraries(helloWorld gtsam)
