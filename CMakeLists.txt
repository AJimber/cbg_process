cmake_minimum_required(VERSION 3.10)

project(cbg_process VERSION 1.8.1 LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

set(CMAKE_CXX_FLAGS_DEBUG "-ggdb3 -O0 -Wall")
set(CMAKE_CXX_FLAGS_RELEASE "-g -O3 -Wall")

find_package(OpenCV REQUIRED)

include_directories(${OpenCV_INCLUDE_DIRS})

add_executable(cbg_process
    cbg_process.cpp
    common_code.cpp
    common_code.hpp
)

target_link_libraries(cbg_process ${OpenCV_LIBS})