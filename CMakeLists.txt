cmake_minimum_required(VERSION 2.8)

project (Lab7-2)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11")

set(HEADERS ${PROJECT_SOURCE_DIR}/include/Lab7-2.h)
set(HEADERS ${PROJECT_SOURCE_DIR}/include/catch.hpp)
set(SOURCES ${PROJECT_SOURCE_DIR}/sources/Lab7-2.cpp)

set(EXECUTABLE_OUTPUT_PATH ${PROJECT_BINARY_DIR}/bin)
set(LIBRARY_OUTPUT_PATH ${PROJECT_BINARY_DIR}/lib)

include_directories(${PROJECT_SOURCE_DIR}/include)

add_library (${PROJECT_NAME} STATIC ${SOURCES})

add_subdirectory(example)
add_subdirectory(tests)
