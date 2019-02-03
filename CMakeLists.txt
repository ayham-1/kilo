cmake_minimum_required(VERSION 3.5)

project(kilo C)

set(CMAKE_C_FLAGS "${CMAKE_C_FLAGS} -O0")
set(CMAKE_C_FLAGS "${CMAKE_C_FLAGS_RELEASE} -g -O0")

set(CMAKE_ARCHIVE_OUTPUT_DIRECTORY "${CMAKE_BINARY_DIR}/bin/")
set(CMAKE_LIBRARY_OUTPUT_DIRECTORY "${CMAKE_BINARY_DIR}/bin/")
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY "${CMAKE_BINARY_DIR}/bin/")

file(GLOB_RECURSE srcs "${CMAKE_SOURCE_DIR}/kilo/*.c")
file(GLOB_RECURSE hdrs "${CMAKE_SOURCE_DIR}/kilo/*.h")

add_executable(kilo ${srcs} ${hdrs})