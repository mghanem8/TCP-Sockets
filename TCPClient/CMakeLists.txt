cmake_minimum_required(VERSION 3.23)
project(TCPServer)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++17")
set(EXECUTABLE_OUTPUT_PATH ../)

set(SOURCE_FILES main.cpp)
add_executable(TCPServer ${SOURCE_FILES})
include_directories(/usr/local/include)

find_package(SFML 2.5 COMPONENTS system window graphics network audio REQUIRED)
include_directories(${SFML_INCLUDE_DIRS})
target_link_libraries(TCPServer sfml-system sfml-window sfml-graphics sfml-audio sfml-network)