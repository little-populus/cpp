cmake_minimum_required(VERSION 3.20.0)

project(c++ VERSION 1.0.0 LANGUAGES C CXX)

set(CMAKE_EXPORT_COMPILE_COMMANDS ON)
set(CMAKE_CXX_STANDARD 20)

add_executable(c++ main.cpp)
add_library(inode_info OBJECT inode_info.cpp)
target_include_directories(inode_info PUBLIC head)
target_link_libraries(c++ PRIVATE inode_info)