cmake_minimum_required(VERSION 3.9)
project(code)

set(CMAKE_CXX_STANDARD 11)

set( CMAKE_BUILD_TYPE "RELEASE" )

find_package( Sophus REQUIRED )
find_package( Pangolin REQUIRED )

include_directories( "/usr/include/eigen3" )
include_directories( ${Sophus_INCLUDE_DIRS} )
include_directories( ${Pangolin_INCLUDE_DIRS} )

add_executable( code draw_trajectory.cpp )
target_link_libraries( code ${Sophus_LIBRARIES} ${Pangolin_LIBRARIES} )