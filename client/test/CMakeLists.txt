cmake_minimum_required(VERSION 3.24)
project(ClientTests VERSION 1.0)

enable_testing()

add_executable(${PROJECT_NAME} tests.cpp)

target_include_directories(${PROJECT_NAME} PUBLIC ${MATH_LIB_INCLUDE_DIRS})
target_link_libraries(${PROJECT_NAME} ${MATH_LIB_LIBRARIES} GTest::gtest_main GTest::gmock_main)

include(GoogleTest)
gtest_discover_tests(${PROJECT_NAME})
