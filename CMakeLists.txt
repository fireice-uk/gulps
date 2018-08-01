cmake_minimum_required(VERSION 2.6)
project(gulps)

add_executable(gulps main.cpp)

install(TARGETS gulps RUNTIME DESTINATION bin)
