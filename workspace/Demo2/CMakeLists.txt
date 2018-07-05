#CMake
cmake_minimum_required(VERSION 2.8)

#PROJ
project(Demo2)

#search cpps
aux_source_directory(. DIR_SRCS)

#
add_executable(Demo2 ${DIR_SRCS})
