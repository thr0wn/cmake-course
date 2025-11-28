set(LIBRARY_SOURCES
    "my_lib.cpp")
set(LIBRARY_HEADERS
    "my_lib.hpp")
set(LIBRARY_INCLUDES
    "./"
    "${CMAKE_BINARY_DIR}/config")

add_library(${LIBRARY_NAME} STATIC
    ${LIBRARY_SOURCES}
    ${LIBRARY_HEADERS})
target_include_directories(${LIBRARY_NAME} PUBLIC
    ${LIBRARY_INCLUDES})
target_link_libraries(${LIBRARY_NAME} PUBLIC
    nlohmann_json::nlohmann_json
    fmt::fmt
    spdlog::spdlog
    cxxopts::cxxopts)

if(ENABLE_WARNINGS)
  target_set_warnings(${LIBRARY_NAME} ${ENABLE_WARNINGS} ${ENABLE_WARNINGS_AS_ERRORS})
endif()

target_compile_definitions(${LIBRARY_NAME} PUBLIC PRINT_HELLO_WORLD)
