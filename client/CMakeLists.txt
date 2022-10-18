cmake_minimum_required(VERSION 3.24)
project(TestCMakeClient VERSION 1.0)

file(GLOB SOURCES "src/*.cpp" "src/**/*.cpp" "src/*.h" "src/**/*.h")

add_subdirectory(vendor/mathlib)

add_executable(${PROJECT_NAME} ${SOURCES})

target_link_libraries(${PROJECT_NAME} PUBLIC TestCMakeVendorMathLib)

target_include_directories(${PROJECT_NAME} PUBLIC MATH_LIB_INCLUDE_DIRS)

add_subdirectory(test)