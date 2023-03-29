cmake_minimum_required(VERSION 3.22)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

project(hello_world)

add_executable(hello_world ${CMAKE_CURRENT_SOURCE_DIR}/ hello_world.cpp)

include_directories(${CMAKE_CURRENT_SOURCE_DIR}/../formatter_ex_lib)
add_subdirectory(${CMAKE_CURRENT_SOURCE_DIR}/../formatter_ex_lib formatter_ex)

target_link_libraries(hello_world formatter_ex)
