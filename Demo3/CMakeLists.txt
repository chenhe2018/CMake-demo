#
cmake_minimum_required(VERSION 2.8)

#PROJ
project(Demo3)

#search cpps
aux_source_directory(. DIR_SRCS)

#add catalog
add_subdirectory(math)

#TARGET
add_executable(Demo3 main.cc)

#add libs
target_link_libraries(Demo3 MathFunctions)
