cmake_minimum_required(VERSION 3.15)
project(opengl_tests)

add_subdirectory(glfw)

include_directories(glfw/include)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -O2 -Wall -Wextra -std=c++11")

add_subdirectory(glad/)

set(SOURCE_FILES main.cpp)

add_executable(opengl_tests ${SOURCE_FILES})

target_link_libraries(opengl_tests
        glad glfw ${GLFW_LIBRARIES} )