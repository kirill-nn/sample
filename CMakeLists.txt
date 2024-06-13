cmake_minimum_required(VERSION 3.25)
project(Sample CXX)

set(CMAKE_CXX_STANDARD 20)

find_package(fmt REQUIRED)

file(GLOB_RECURSE SOURCES src/*.cpp)

add_executable(${PROJECT_NAME} ${SOURCES})

target_link_libraries(${PROJECT_NAME} PRIVATE
        fmt::fmt-header-only
)

# setup unit tests
enable_testing()

find_package(GTest CONFIG REQUIRED)

file(GLOB_RECURSE TEST_SOURCES test/*.cpp)

add_executable(${PROJECT_NAME}Tests ${TEST_SOURCES})

target_link_libraries(${PROJECT_NAME}Tests PRIVATE
        fmt::fmt-header-only
        GTest::gtest
        GTest::gtest_main
        GTest::gmock
        GTest::gmock_main)