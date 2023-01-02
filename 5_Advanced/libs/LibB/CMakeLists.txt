cmake_minimum_required(VERSION 3.1)

set(PROJECT_NAME
    LibB
)
set(LIBRARY_NAME
    LibB
)

file(GLOB PRIVATE_SOURCE
    "src/*.cpp"
)
file(GLOB PRIVATE_HEADES
    "src/*.h"
)
file(GLOB HEADERS 
    RELATIVE include/${LIBRARY_NAME}
    "include/*.h"
)

project(${PROJECT_NAME})

add_library(${LIBRARY_NAME} STATIC
    ${HEADERS}
    ${PRIVATE_HEADER}
    ${PRIVATE_SOURCE}
)

target_include_directories(${LIBRARY_NAME} PRIVATE
    $<BUILD_INTERFACE:${CMAKE_CURRENT_SOURCE_DIR}/include/${LIBRARY_NAME}>
    $<INSTALL_INTERFACE:include/${LIBRARY_NAME}>
)

target_include_directories(${LIBRARY_NAME} PUBLIC
    $<BUILD_INTERFACE:${CMAKE_CURRENT_SOURCE_DIR}/include>
    $<INSTALL_INTERFACE:include>
)
