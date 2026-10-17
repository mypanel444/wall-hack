cmake_minimum_required(VERSION 3.18)
project(longrange)
set(CMAKE_CXX_STANDARD 17)
set(CMAKE_POSITION_INDEPENDENT_CODE ON)

# Isama si Dobby dito
add_subdirectory(Dobby)

add_library(longrange SHARED main.cpp)

target_link_libraries(longrange
    log
    android
    dl
    pthread
    dobby
)
