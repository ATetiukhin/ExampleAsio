cmake_minimum_required(VERSION 3.3)
project(BoostTest)

set(Boost_USE_STATIC_LIBS        ON)
set(Boost_USE_MULTITHREADED      ON)
set(Boost_USE_STATIC_RUNTIME    OFF)

find_package(Boost 1.64.0 COMPONENTS date_time system regex REQUIRED)
if (Boost_FOUND)
    include_directories(${Boost_INCLUDE_DIRS})
    # link_directories(${Boost_LIBRARY_DIRS})
endif()

add_executable(AsioTest main.cpp)
target_link_libraries(AsioTest ${Boost_LIBRARIES})