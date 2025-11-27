add_executable(executable main.cpp)
target_link_libraries(executable PUBLIC library)
add_subdirectory(my-lib)
