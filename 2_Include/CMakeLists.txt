cmake_minimum_required(VERSION 3.1)

project(
    LearningCMake
    VERSION 1.0
    LANGUAGES CXX
)

add_executable(HelloInclude main.cpp hello.h hello.cpp)