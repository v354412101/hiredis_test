cmake_minimum_required(VERSION 3.14)
project(hiredistest C)

set(CMAKE_C_STANDARD 99)
set(CMAKE_BUILD_TYPE Debug)

include_directories(${PROJECT_SOURCE_DIR}/3rdparty/libevent/include)
link_libraries(${PROJECT_SOURCE_DIR}/3rdparty/libevent/lib/libevent.a)

include_directories(${PROJECT_SOURCE_DIR}/3rdparty/hiredis/include)
link_libraries(${PROJECT_SOURCE_DIR}/3rdparty/hiredis/lib/libhiredis.a)

add_executable(hiredis_test src/main.c)