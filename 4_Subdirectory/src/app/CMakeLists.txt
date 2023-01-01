cmake_minimum_required(VERSION 3.1)

include_directories(${CMAKE_SOURCE_DIR}/src)

add_executable(SimpleProject main.cpp)
target_link_libraries(SimpleProject PRIVATE MyHelloLib)