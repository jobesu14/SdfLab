cmake_minimum_required(VERSION 3.0.0)
project(SdfLab VERSION 0.1.0)

include(CTest)
enable_testing()

add_library(
    sdf-lab
    src/SdfLab/SdfLab.hpp
    src/SdfLab/SdfLab.cpp
    )

target_include_directories(sdf-lab PUBLIC "${CMAKE_CURRENT_SOURCE_DIR}/src")

set(CPACK_PROJECT_NAME ${PROJECT_NAME})
set(CPACK_PROJECT_VERSION ${PROJECT_VERSION})
include(CPack)
