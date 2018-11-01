cmake_minimum_required(VERSION 3.5 FATAL_ERROR)

include(gtest.cmake)

set(CMAKE_CXX_FLAGS)

set(UNITTESTING_VERSION_MAJOR 1)
set(UNITTESTING_VERSION_MINOR 0)
set(LEARN_CMAKE_VERSION_PATCH 0)

set(CMAKE_BUILD_TYPE Debug)

project(TravisBuild)
enable_testing()

SET(TARGET_SRC ./TravisTest.cpp)

add_executable(TravisBuild ${TARGET_SRC})

find_package (Threads)
target_link_libraries(BuildTravisCI gtest ${CMAKE_THREAD_LIBS_INIT})