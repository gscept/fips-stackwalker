#
# project: fips-stackwalker/
#
cmake_minimum_required(VERSION 3.21)

if (NOT FIPS_IMPORT)
# include the fips main cmake file
get_filename_component(FIPS_ROOT_DIR "../fips" ABSOLUTE)
include("${FIPS_ROOT_DIR}/cmake/fips.cmake")
project(fips-stackwalker)
fips_setup()
endif()

include_directories(StackWalker/Main)


fips_begin_lib(StackWalker)
fips_dir(StackWalker/Main/StackWalker StackWalker)
fips_files(StackWalker.h StackWalker.cpp)
fips_end_lib()
