set(MAIN_SRC main.cpp)

add_executable(main ${MAIN_SRC})
target_link_libraries(main hello)

set(CMAKE_INCLUDE_PATH ${PROJECT_SOURCE_DIR})
find_path(HELLO_INCLUDE_DIR hello.h PATHS ${CMAKE_INCLUDE_PATH} ${CMAKE_INCLUDE_PATH}/lib)
if(HELLO_INCLUDE_DIR)
    message(STATUS "hello.h is located in ${HELLO_INCLUDE_DIR}")
    target_include_directories(main PRIVATE ${HELLO_INCLUDE_DIR})
else()
    message(FATAL_ERROR "cannot find hello.h")
endif(HELLO_INCLUDE_DIR)