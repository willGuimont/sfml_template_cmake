cmake_minimum_required(VERSION 3.16)
project(sfml_test)

set(CMAKE_CXX_STANDARD 20)

set(EXECUTABLE_NAME "sfml_template")
add_executable(${EXECUTABLE_NAME} main.cpp)

message(${CMAKE_SOURCE_DIR})

set(CMAKE_MODULE_PATH "${CMAKE_SOURCE_DIR}/cmake_modules" ${CMAKE_MODULE_PATH})
find_package(SFML 2 REQUIRED system window graphics network audio)
target_link_libraries(${EXECUTABLE_NAME} ${SFML_LIBRARIES})
