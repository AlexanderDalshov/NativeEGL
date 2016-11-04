cmake_minimum_required(VERSION 3.4)

add_subdirectory(spdlog)

project(UV)
set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

set(SOURCE_FILES
    uv.cpp
    )

add_library(uv SHARED ${SOURCE_FILES})
target_link_libraries(uv log android spdlog)

