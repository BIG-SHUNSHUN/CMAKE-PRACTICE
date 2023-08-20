cmake_minimum_required(VERSION 3.11)

project(hello)

set(CMAKE_INSTALL_PREFIX ${PROJECT_SOURCE_DIR}/install)

add_subdirectory(lib)
add_subdirectory(src)

message(STATUS "CMake major version: ${CMAKE_MAJOR_VERSION}")
message(STATUS "CMake minor version: ${CMAKE_MINOR_VERSION}")
message(STATUS "CMake patch version: ${CMAKE_PATCH_VERSION}")
message(STATUS "system: ${CMAKE_SYSTEM}")
message(STATUS "system name: ${CMAKE_SYSTEM_NAME}")
message(STATUS "system version: ${CMAKE_SYSTEM_VERSION}")
message(STATUS "processor: ${CMAKE_SYSTEM_PROCESSOR}")
message(STATUS "is unix: ${UNIX}")
message(STATUS "is windows: ${WIN32}")