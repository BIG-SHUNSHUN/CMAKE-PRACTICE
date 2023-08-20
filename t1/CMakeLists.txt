cmake_minimum_required(VERSION 3.11)

project(HELLO VERSION 1.2)

message(FATAL_ERROR "THIS is BINARY dir: " ${HELLO_BINARY_DIR})
message(STATUS "THIS is SOURCE dir: " ${HELLO_SOURCE_DIR})

message(STATUS "major version: " ${PROJECT_VERSION_MAJOR})
message(STATUS "minor version: " ${PROJECT_VERSION_MINOR})
message(STATUS "project version: ${PROJECT_VERSION_MAJOR}.${PROJECT_VERSION_MINOR}")

set(SRC_LIST main.cpp)

add_executable(hello ${SRC_LIST})