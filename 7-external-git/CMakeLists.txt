cmake_minimum_required(VERSION 3.22)
project(external-git VERSION 1.0.0 LANGUAGES C CXX)
set(CMAKE_EXPORT_COMPILE_COMMANDS ON)

set(CMAKE_CXX_STANDARD             17)
set(CMAKE_CXX_STANDARD_REQUIRED    ON)
set(CMAKE_CXX_STANDARD_EXTENSIONS OFF)

set(LIBRARY_NAME library)
set(EXECUTABLE_NAME executable)

set(CMAKE_MODULE_PATH "${PROJECT_SOURCE_DIR}/cmake/")
include(AddGitSubmodule)

add_git_submodule(external/json)

add_subdirectory(src)
add_subdirectory(external)
add_subdirectory(config)
add_subdirectory(app)
