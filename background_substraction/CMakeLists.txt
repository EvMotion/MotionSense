cmake_minimum_required(VERSION 3.26)

# Project name
project(EventSight)

# Specify the required C++ standard
set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED True)

# Find OpenCV 4 package
find_package(OpenCV 4 REQUIRED)

# Add the executable
add_executable(EventSight background_substractor.cpp)

# Include OpenCV directories
target_include_directories(EventSight PRIVATE ${OpenCV_INCLUDE_DIRS})

# Link the executable with the OpenCV libraries
target_link_libraries(EventSight ${OpenCV_LIBS})
