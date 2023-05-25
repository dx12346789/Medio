cmake_minimum_required(VERSION 3.25)
project(Medio)

file(GLOB_RECURSE MEDIO_SOURCES ${CMAKE_CURRENT_SOURCE_DIR}/*.cpp)

add_executable(${PROJECT_NAME} ${MEDIO_SOURCES})
