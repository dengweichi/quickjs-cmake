cmake_minimum_required(VERSION 3.5.1)
project(quickjs-cmake)

if(CMAKE_SYSTEM_NAME STREQUAL "Linux")
    add_definitions(-D__linux__)
elseif(CMAKE_SYSTEM_NAME STREQUAL "Darwin")
    add_definitions(-D__APPLE__)
elseif(CMAKE_SYSTEM_NAME STREQUAL "Windows")
    add_definitions(-D_WIN32)
endif()

# 定义大数字
add_definitions(-DCONFIG_BIGNUM)