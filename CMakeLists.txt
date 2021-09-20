cmake_minimum_required(VERSION 3.13.0 FATAL_ERROR)
project(boost-gtest-link-error)

add_executable(exec)
target_sources(exec
    PRIVATE
        src/main.cpp
)

find_package(Boost REQUIRED)
find_package(GTest REQUIRED)

target_link_libraries(exec
    PRIVATE
        Boost::Boost
        GTest::GTest
)
