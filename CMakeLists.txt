cmake_minimum_required(VERSION 3.22)

project(libcanard LANGUAGES C)
set(CMAKE_C_STANDARD 11)

add_library(libcanard STATIC
    "libcanard/canard.c"
)
set_target_properties(libcanard PROPERTIES POSITION_INDEPENDENT_CODE ON)

target_include_directories(libcanard
    PUBLIC
        $<BUILD_INTERFACE:${CMAKE_CURRENT_SOURCE_DIR}/libcanard>
        $<INSTALL_INTERFACE:include/libcanard>
)
