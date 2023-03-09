cmake_minimum_required(VERSION 3.5)

project(homework-lab01 LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

add_executable(homework-lab01 main.cpp)

install(TARGETS homework-lab01
    LIBRARY DESTINATION ${CMAKE_INSTALL_LIBDIR})
