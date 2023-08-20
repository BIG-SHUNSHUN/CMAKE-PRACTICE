set(HELLO_SRC hello.cpp)

add_library(hello_static STATIC ${HELLO_SRC})
add_library(hello SHARED ${HELLO_SRC})

set_target_properties(hello_static PROPERTIES OUTPUT_NAME hello)
set_target_properties(hello PROPERTIES VERSION 1.2)

install(TARGETS hello hello_static 
                LIBRARY DESTINATION lib/
                ARCHIVE DESTINATION lib/)
install(FILES hello.h DESTINATION include/hello)