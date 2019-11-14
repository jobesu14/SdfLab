cmake_minimum_required(VERSION 3.0.0)
project(SdfLab VERSION 0.1.0)

include(CTest)
enable_testing()

add_subdirectory(src/cmd_line_tool)
add_subdirectory(libs/gflags)

add_library(
    sdf-lab
    src/SdfLab/SdfLab.hpp
    src/SdfLab/SdfLab.cpp
    )
target_include_directories(sdf-lab PUBLIC "${CMAKE_CURRENT_SOURCE_DIR}/src")

add_library(
	obj_io
	libs/obj_io/obj_io.hpp
	libs/obj_io/obj_io.cpp
	)
target_include_directories(obj_io PUBLIC "${CMAKE_CURRENT_SOURCE_DIR}/libs")


set(CPACK_PROJECT_NAME ${PROJECT_NAME})
set(CPACK_PROJECT_VERSION ${PROJECT_VERSION})
include(CPack)
