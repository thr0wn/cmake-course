cmake_minimum_required(VERSION 3.22)

project(basic-poject VERSION 1.0.0 LANGUAGES C CXX)

add_library(library STATIC src/my_lib.cpp)

add_executable(executable src/main.cpp)

target_link_libraries(executable PUBLIC library)
