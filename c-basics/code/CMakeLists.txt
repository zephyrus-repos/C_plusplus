cmake_minimum_required(VERSION 3.13) # minimum required version of CMake

project("c-basics" CXX)
add_library(${PROJECT_NAME} INTERFACE) # interface library target named "c-basics"

set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_EXTENSIONS Off)
set(CMAKE_CXX_STANDARD_REQUIRED On)
set(CMAKE_EXPORT_COMPILE_COMMANDS On)

list(APPEND CMAKE_MODULE_PATH "${CMAKE_CURRENT_SOURCE_DIR}/config/cmake")

# enable testing for the project
enable_testing()
# include CTest module for testing support
include(CTest)

include(add-targets)

include_directories(include)

add_subdirectory(source)
add_subdirectory(test)
#add_subdirectory(solutions)
