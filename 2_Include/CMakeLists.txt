cmake_minimum_required(VERSION 3.25)

project(
    HelloInclude
    VERSION 1.0
    LANGUAGES CXX
)

add_executable(HelloInclude main.cpp hello.h hello.cpp)