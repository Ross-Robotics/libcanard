cmake_minimum_required(VERSION 3.28)

project(libcanard LANGUAGES C)
set(CMAKE_C_STANDARD 11)

add_library(libcanard STATIC
    "libcanard/canard.c"
)

target_include_directories(libcanard
    PUBLIC
        "${CMAKE_CURRENT_SOURCE_DIR}/libcanard"
)
