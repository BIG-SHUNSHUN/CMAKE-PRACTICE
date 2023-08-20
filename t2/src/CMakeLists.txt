set(EXECUTABLE_OUTPUT_PATH ${PROJECT_BINARY_DIR}/bin/)
add_executable(hello main.cpp)

install(TARGETS hello DESTINATION ${PROJECT_SOURCE_DIR}/install/bin)