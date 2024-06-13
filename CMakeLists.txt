cmake_minimum_required(VERSION 3.29.4)

project(demo-cmake-mingw)

set(CMAKE_GENERATOR "MinGW Makefiles")

add_library(add STATIC src/lib/add.cpp)

add_executable(main src/main.cpp)

target_include_directories(main PRIVATE src/include)

target_link_libraries(main add)