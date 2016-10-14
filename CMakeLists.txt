# CMakeLists.txt

cmake_minimum_required(VERSION 2.8.7)



project(hello_world)

include_directories(${CMAKE_CURRENT_SOURCE_DIR}/include/)

add_library(hello STATIC ${CMAKE_CURRENT_SOURCE_DIR}/sources/print_hello_world.cpp)

add_executable(example ${CMAKE_CURRENT_SOURCE_DIR}/examples/main.cpp)

target_link_libraries(example hello) 
