cmake_minimum_required(VERSION 3.22)
project(fetch-content VERSION 1.0.0 LANGUAGES C CXX)
set(CMAKE_EXPORT_COMPILE_COMMANDS ON)

set(CMAKE_CXX_STANDARD             17)
set(CMAKE_CXX_STANDARD_REQUIRED    ON)
set(CMAKE_CXX_STANDARD_EXTENSIONS OFF)

set(LIBRARY_NAME library)
set(EXECUTABLE_NAME executable)

set(CMAKE_MODULE_PATH "${PROJECT_SOURCE_DIR}/cmake/")

include(FetchContent)

FetchContent_Declare (
  nlohmann_json
  GIT_REPOSITORY https://github.com/nlohmann/json
  GIT_TAG v3.11.2
  GIT_SHALLOW TRUE
)
FetchContent_MakeAvailable(nlohmann_json)

add_subdirectory(src)
add_subdirectory(config)
add_subdirectory(app)
