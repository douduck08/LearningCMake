cmake_minimum_required(VERSION 3.25)

# Variables
set(PROJECT_NAME
    AdvancedProject
)

set(SOURCE_DIR
    src
)
set(SOURCE
    ${SOURCE_DIR}/main.cpp
)

set(LIBRARIES_DIR
    libs
)
set(LIBRARIES
    LibA
    LibB
)

# Project
project(
    ${PROJECT_NAME}
    VERSION 1.0
    LANGUAGES CXX
)

foreach(LIBRARY ${LIBRARIES})
    add_subdirectory(${LIBRARIES_DIR}/${LIBRARY})
endforeach()

add_executable(${PROJECT_NAME} ${SOURCE})
target_link_libraries(${PROJECT_NAME} ${LIBRARIES})