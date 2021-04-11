###############################################
#
# Top-level CMakeLists file for lrose-cnvgrb
#
###############################################

cmake_minimum_required(VERSION 3.0)

project (lrose-cnvgrb)

set(CMAKE_C_COMPILER_NAMES clang gcc icc cc)

set(CMAKE_VERBOSE_MAKEFILE TRUE)

set(FETCHCONTENT_QUIET false CACHE BOOL "" FORCE)

set(PACKAGE "LROSE-CNVGRB" CACHE STRING "")

# Finding pkg-config
find_package(PkgConfig REQUIRED)

# If user did not provide CMAKE_INSTALL_PREFIX, use ~/lrose
if(CMAKE_INSTALL_PREFIX_INITIALIZED_TO_DEFAULT)
  set(CMAKE_INSTALL_PREFIX "$ENV{HOME}/lrose" CACHE PATH "..." FORCE)
endif()
message("CMAKE_INSTALL_PREFIX is ${CMAKE_INSTALL_PREFIX}")

enable_testing()

# Set RPATH so that executable finds libraries
# without needing LD_LIBRARY_PATH

set(CMAKE_SKIP_BUILD_RPATH FALSE)
set(CMAKE_BUILD_WITH_INSTALL_RPATH TRUE)

set(CMAKE_INSTALL_RPATH ${CMAKE_INSTALL_PREFIX}/lib)
set(CMAKE_INSTALL_RPATH_USE_LINK_PATH TRUE)

if(${CMAKE_SYSTEM_NAME} MATCHES "Linux")
  set(CMAKE_EXE_LINKER_FLAGS "-Wl,--enable-new-dtags")
endif()

add_subdirectory(src)
