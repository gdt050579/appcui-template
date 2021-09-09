cmake_minimum_required(VERSION 3.13)

# Project setup
project(SimpleWin VERSION 1.0)

set_property(GLOBAL PROPERTY USE_FOLDERS ON)

set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED True)

set(CMAKE_ARCHIVE_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/../bin)
set(CMAKE_LIBRARY_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/../bin)
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/../bin)

add_executable(SimpleWin src/main.cpp)

add_subdirectory(AppCUI)

target_include_directories(SimpleWin PUBLIC AppCUI)

target_link_libraries(SimpleWin PUBLIC AppCUI)



