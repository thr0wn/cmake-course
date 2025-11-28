cmake_minimum_required(VERSION 3.22)
project(configure-file VERSION 1.0.0 LANGUAGES C CXX)
set(CMAKE_EXPORT_COMPILE_COMMANDS ON)

set(CMAKE_CXX_STANDARD             17)
set(CMAKE_CXX_STANDARD_REQUIRED    ON)
set(CMAKE_CXX_STANDARD_EXTENSIONS OFF)

set(LIBRARY_NAME library)
set(EXECUTABLE_NAME executable)

option(COMPILE_EXECUTABLE "Whether to compile the executable" ON)

add_subdirectory(src)
add_subdirectory(config)
if(COMPILE_EXECUTABLE)
  add_subdirectory(app)
else()
  message("W/o exe. compiling")
endif()
