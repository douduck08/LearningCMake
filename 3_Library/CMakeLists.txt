cmake_minimum_required(VERSION 3.1)

project(
    LearningCMake
    VERSION 1.0
    LANGUAGES CXX
)

add_library(MyHelloLib hello.h hello.cpp)

add_executable(HelloLibrary main.cpp)

target_link_libraries(HelloLibrary PRIVATE MyHelloLib)