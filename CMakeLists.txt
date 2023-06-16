cmake_minimum_required(VERSION 3.12)

project(NAMCoreFastWavenet)

# Set C++ standard to C++17
set(CMAKE_CXX_STANDARD 17)
# set(CMAKE_CXX_STANDARD_REQUIRED ON)
# set(CMAKE_CXX_EXTENSIONS OFF)

# Create an executable for your project
add_executable(NAMCoreFastWavenet)

target_sources(NAMCoreFastWavenet PUBLIC testrun.cpp)