#
cmake_minimum_required (VERSION 2.8)

#PROJ
project(Demo4)

#add a configure file
configure_file(
  "${PROJECT_SOURCE_DIR}/config.h.in"
  "${PROJECT_BINARY_DIR}/config.h"
)

#judge if my libs are activated
option(USE_MYMATH
       "Use provided math implementation" ON)

#if lib:MathFunctions work?
if(USE_MYMATH)
  include_directories("${PROJECT_SOURCE_DIR}/math")
  add_subdirectory(math)
  set(EXTRA_LIBS ${EXTRA_LIBS} MathFunctions)
endif(USE_MYMATH)

# search cpps
aux_source_directory(. DIR_SRCS)

#TARGET
add_executable(Demo4 ${DIR_SRCS})
target_link_libraries(Demo4 ${EXTRA_LIBS})
