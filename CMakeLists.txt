cmake_minimum_required(VERSION 4.3)
project(cpp_thread_pool VERSION 0.1.0 LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_EXTENSIONS OFF)

add_library(cpp_thread_pool INTERFACE)
target_include_directories(cpp_thread_pool INTERFACE include)

add_executable(ThreadPoolExample examples/main.cpp)
target_link_libraries(ThreadPoolExample PRIVATE cpp_thread_pool)

add_executable(ThreadPoolTest tests/test_main.cpp)
target_link_libraries(ThreadPoolTest PRIVATE cpp_thread_pool)