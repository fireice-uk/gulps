cmake_minimum_required(VERSION 2.6)
project(gulps)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

set(CMAKE_THREAD_PREFER_PTHREAD TRUE)
set(THREADS_PREFER_PTHREAD_FLAG TRUE)
find_package(Threads REQUIRED)

add_definitions(-DFMT_EXTENDED_COLORS)
add_executable(gulps main.cpp fmt/format.cc fmt/posix.cc)
target_link_libraries(gulps Threads::Threads)

target_include_directories(gulps PRIVATE ".")

install(TARGETS gulps RUNTIME DESTINATION bin)
