cmake_minimum_required(VERSION 3.0)
project(interpolation-methods)

set(CMAKE_CXX_STANDARD 11)

option(INTERPOL_BUILD_APP_RUNTIME_EXPERIMENTS "Build Runtime Experiments" ON)
option(INTERPOL_BUILD_VIZ "Build Visualization" ON)

add_subdirectory(libinterpol)

if(INTERPOL_BUILD_APP_RUNTIME_EXPERIMENTS)
    add_subdirectory(app_runtime)
endif()

if(INTERPOL_BUILD_VIZ)
    add_subdirectory(libinterpolviz)
    add_subdirectory(app_visualization)
endif()