add_executable(main main.cpp)

set(CMAKE_MODULE_PATH ${PROJECT_SOURCE_DIR}/cmake)
find_package(HELLO REQUIRED)
if(HELLO_FOUND)
    target_include_directories(main PRIVATE ${HELLO_INCLUDE_DIR})
    target_link_libraries(main ${HELLO_LIBRARY})
endif()