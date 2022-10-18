cmake_minimum_required(VERSION 3.24)
project(TestCMake VERSION 1.0)

set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

include(FetchContent)

FetchContent_Declare(
    googletest
    GIT_REPOSITORY https://github.com/google/googletest.git
    GIT_TAG release-1.12.1
    FIND_PACKAGE_ARGS NAMES GTest
)

FetchContent_MakeAvailable(googletest)


add_subdirectory(client)