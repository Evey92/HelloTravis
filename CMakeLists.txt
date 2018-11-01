cmake_minimum_required(VERSION 3.5 FATAL_ERROR)
include(gtest.cmake)

project(BuildTravisCI)

set(CMAKE_CXX_FLAGS)

set(CMAKE_BUILD_TYPE Debug)

set(TARGET_SRC ./TravisTest.cpp)

add_executable(BuildTravisCI ${TARGET_SRC})

find_package (Threads)
target_link_libraries(BuildTravisCI gtest ${CMAKE_THREAD_LIBS_INIT})