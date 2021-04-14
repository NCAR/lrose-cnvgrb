###############################################
#
# CMakeLists.txt file for cnvgrb
#
###############################################

project (cnvgrb)

# source files

set (SRCS
  gds2gdt.f
  pds2pdt.f
  pds2pdtens.f
  cnvgrib.f
  cnv12.f
  cnv22.f
  cnv21.f
  gdt2gds.f
  makepds.f
  putgbexn.f
  makepdsens.f
  setbit.f
    )

# include directories

include_directories (${CMAKE_CURRENT_BINARY_DIR}/../g2lib-3.2.0)
include_directories (${CMAKE_CURRENT_BINARY_DIR}/../w3lib-2.2.0)
include_directories (${CMAKE_INSTALL_PREFIX}/include)

# link directories

link_directories (${CMAKE_CURRENT_BINARY_DIR}/../g2lib-3.2.0)
link_directories (${CMAKE_CURRENT_BINARY_DIR}/../w3lib-2.2.0)
link_directories (${CMAKE_INSTALL_PREFIX}/lib)

# link libs

link_libraries (g2)
link_libraries (w3)
link_libraries (jasper)
link_libraries (png)
link_libraries (z)

add_executable (${PROJECT_NAME} ${SRCS})

# install

INSTALL(TARGETS ${PROJECT_NAME}
        DESTINATION ${CMAKE_INSTALL_PREFIX}/bin
       )

