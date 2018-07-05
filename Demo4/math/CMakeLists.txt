#search cpps
aux_source_directory(. DIR_LIB_SRCS)

#generate libs
add_library(MathFunctions ${DIR_LIB_SRCS})
