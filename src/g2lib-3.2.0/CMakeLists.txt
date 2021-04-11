# CMakeLists for AparData library

project (g2)

set (SRCS
  addfield.f
  addgrid.f
  addlocal.f
  cmplxpack.f
  compack.f
  comunpack.f
  dec_jpeg2000.c
  dec_png.c
  drstemplates.f
  enc_jpeg2000.c
  enc_png.c
  g2_gbytesc.f
  g2grids.f
  gb_info.f
  gdt2gds.f
  getdim.f
  getfield.f
  getg2i.f
  getg2ir.f
  getgb2.f
  getgb2l.f
  getgb2p.f
  getgb2r.f
  getgb2rp.f
  getgb2s.f
  getidx.f
  getidxes.f
  getlocal.f
  getpoly.f
  gettemplates.f
  gf_free.f
  gf_getfld.f
  gf_unpack1.f
  gf_unpack2.f
  gf_unpack3.f
  gf_unpack4.f
  gf_unpack5.f
  gf_unpack6.f
  gf_unpack7.f
  grib2.doc
  gribcreate.f
  gribend.f
  gribinfo.f
  gribmod.f
  gridtemplates.f
  intmath.f
  ixgb2.f
  jpcpack.f
  jpcunpack.f
  makefile
  misspack.f
  mkieee.f
  mova2i.c
  pack_gp.f
  params.f
  params_ecmwf.f
  pdstemplates.f
  pngpack.f
  pngunpack.f
  putgb2.f
  rdieee.f
  realloc.f
  reduce.f
  simpack.f
  simunpack.f
  skgb.f
  specpack.f
  specunpack.f
  )

set(CMAKE_Fortran_FLAGS "-fno-range-check")

add_library (${PROJECT_NAME} ${SRCS})

INSTALL(TARGETS ${PROJECT_NAME}
        DESTINATION ${CMAKE_INSTALL_PREFIX}/lib
       )

