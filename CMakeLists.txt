#
# project: fips-stackwalker/
#
cmake_minimum_required(VERSION 2.8)

# include the fips main cmake file
get_filename_component(FIPS_ROOT_DIR "../fips" ABSOLUTE)
include("${FIPS_ROOT_DIR}/cmake/fips.cmake")

include_directories(StackWalker/Main)

fips_setup(PROJECT fips-stackwalker/)
fips_project(StackWalker)
fips_begin_lib(StackWalker)
fips_dir(StackWalker/Main/StackWalker StackWalker)
fips_files(StackWalker.h StackWalker.cpp)
fips_end_lib()
fips_finish()
