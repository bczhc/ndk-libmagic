CMAKE_MINIMUM_REQUIRED(VERSION 3.10.0)

set(CMAKE_C_FLAGS "${CMAKE_C_FLAGS} -Wall -DHAVE_CONFIG_H")
file(GLOB_RECURSE NATIVE_SRCS "src/*.c")
add_library(magic SHARED ${NATIVE_SRCS})
target_link_libraries(magic z)
