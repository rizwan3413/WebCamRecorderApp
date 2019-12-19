cmake_minimum_required(VERSION 2.8)

project(WCR)


# Enable C++11 standard
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11 -Wall")

# public includes/api
include_directories("/usr/local/include/opencv4")

link_directories("/usr/local/lib")

file(GLOB SOURCES "WebCamRecorder.cpp")

add_executable(${PROJECT_NAME} ${SOURCES})

target_link_libraries(${PROJECT_NAME} opencv_core opencv_videoio opencv_highgui)

install(TARGETS ${PROJECT_NAME} DESTINATION bin)


