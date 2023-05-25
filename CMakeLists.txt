cmake_minimum_required(VERSION 3.25)
project(Medio_ALL VERSION 1.0.0)

set(CMAKE_C_STANDARD 17)
set(CMAKE_CXX_STANDARD 17)

# system
if(NOT COMPILE_OS_TYPE)
    if(CMAKE_SYSTEM_NAME MATCHES "Android")
        set(COMPILE_OS_TYPE ANDROID)
    elseif(IOS)
        set(COMPILE_OS_TYPE IOS)
    elseif(CMAKE_SYSTEM_NAME STREQUAL "Linux")
        set(COMPILE_OS_TYPE LINUXOS)
    elseif(CMAKE_SYSTEM_NAME MATCHES "Windows")
        set(COMPILE_OS_TYPE WIN32)
    elseif(CMAKE_SYSTEM_NAME MATCHES "Darwin")
        set(COMPILE_OS_TYPE MACOS)
    endif()
endif()

add_subdirectory(${CMAKE_CURRENT_SOURCE_DIR}/libMedio "libMedio")