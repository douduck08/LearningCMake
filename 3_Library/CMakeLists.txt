cmake_minimum_required(VERSION 3.25)

project(
    HelloLibrary
    VERSION 1.0
    LANGUAGES CXX
)

add_library(HelloLib hello.h hello.cpp)

add_executable(HelloLibrary main.cpp)
target_link_libraries(HelloLibrary PRIVATE MyHelloLib)