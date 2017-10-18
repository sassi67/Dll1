project(Dll1)
cmake_minimum_required(VERSION 2.8.12)
add_definitions("-std=c++11")

include(${CMAKE_BINARY_DIR}/conanbuildinfo.cmake)
conan_basic_setup()

add_library(Dll1 SHARED *.cpp *.h)
target_link_libraries(Dll1 ${CONAN_LIBS})