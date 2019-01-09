cmake_minimum_required(VERSION 2.8)

set(CMAKE_C_FLAGS "${CMAKE_C_FLAGS} -fsanitize=address -O1 -fno-omit-frame-pointer -g")
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -fsanitize=address -O1 -fno-omit-frame-pointer -g -std=c++11")

# Use ASan
add_executable(example example.c)


set(CMAKE_C_FLAGS "-O1 -g")
set(CMAKE_CXX_FLAGS "-O1 -g -std=c++11")

# Without ASan
add_executable(example_without example.c)
