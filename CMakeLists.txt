cmake_minimum_required(VERSION 2.4.8)
project(opencv)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11")
set(CMAKE_BUILD_TYPE Release)
set(OpenCV_DIR "/usr/local/opencv2.4.13")
find_package( OpenCV  REQUIRED )

INCLUDE_DIRECTORIES(${OPENCV_INCLUDE_DIRS})

set(SOURCE_FILES stereo_calib_match.cpp)
add_executable(opencv ${SOURCE_FILES})
target_link_libraries(opencv ${OpenCV_LIBS})
