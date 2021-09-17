cmake_minimum_required(VERSION 3.13.0 FATAL_ERROR)

add_library(lib STATIC)

target_sources(lib
    PUBLIC
        include/lib/header.h
    PRIVATE
        src/source.cpp
)

find_package(Boost REQUIRED)

target_link_libraries(lib
    PRIVATE
        Boost:Boost
)

