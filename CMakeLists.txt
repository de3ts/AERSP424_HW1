cmake_minimum_required(VERSION 3.23) # Specify CMake version.
project(HW_1_AERSP424) # A project name. This can be anything.

set(CMAKE_CXX_STANDARD 20) # Specify C++ version.

# Accessing CMake variables can be done using ${VARIABLE_NAME}.
message(STATUS "CMakeLists.txt is at ${PROJECT_SOURCE_DIR}") # To print something.

# This include a directory.
# Typically, where header files are stored.
# CMAKE_SOURCE_DIR is another variable that CMake automatically created.
# This one is a path to the folder where CMakeList.txt is located.
include_directories(${CMAKE_SOURCE_DIR}/include)

# Create a binary file. 
# The first argument is the name of the binary file.
# It can be anything. In this case, it is set to be the project name.
# The other arguments are source files.
# Header files are not needed in add_executable(), assuming they are properly included.
add_executable(${CMAKE_PROJECT_NAME} ${CMAKE_SOURCE_DIR}/main.cpp)