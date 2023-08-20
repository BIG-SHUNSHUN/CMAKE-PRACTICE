cmake_minimum_required(VERSION 3.11)

project(HELLO VERSION 1.2)

message(STATUS "THIS is BINARY dir: " ${HELLO_BINARY_DIR})
message(STATUS "THIS is SOURCE dir: " ${HELLO_SOURCE_DIR})

message(STATUS "major version: " ${PROJECT_VERSION_MAJOR})
message(STATUS "minor version: " ${PROJECT_VERSION_MINOR})
message(STATUS "project version: ${PROJECT_VERSION_MAJOR}.${PROJECT_VERSION_MINOR}")

add_subdirectory(src)

install(FILES COPYRIGHT README DESTINATION ${PROJECT_SOURCE_DIR}/install/share/doc/cmake/t2)
install(FILES README DESTINATION ${PROJECT_SOURCE_DIR}/install/share/doc/cmake/t2)
install(DIRECTORY doc/ DESTINATION ${PROJECT_SOURCE_DIR}/install/share/doc/cmake/t2)
install(PROGRAMS runHello.sh DESTINATION ${PROJECT_SOURCE_DIR}/install/bin)