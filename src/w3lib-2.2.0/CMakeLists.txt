# CMakeLists for AparData library

project (w3)

set (SRCS
  bacio.v1.3.c
  bacio_module.f
  baciof.f
  errexit.f
  errmsg.f
  fparsei.f
  fparser.f
  gbyte.f
  gbytes_char.f
  getbit.f
  getgb.f
  getgb1r.f
  getgb1re.f
  getgb1s.f
  getgbe.f
  getgbeh.f
  getgbem.f
  getgbemh.f
  getgbemp.f
  getgbens.f
  getgbep.f
  getgbex.f
  getgbexm.f
  getgbh.f
  getgbm.f
  getgbmh.f
  getgbmp.f
  getgbp.f
  getgi.f
  getgir.f
  idsdef.f
  instrument.f
  iw3jdn.f
  ixgb.f
  lengds.f
  mova2i.c
  mova2i.f
  pdsens.f
  pdseup.f
  putgb.f
  putgbe.f
  putgben.f
  putgbens.f
  putgbex.f
  putgbn.f
  r63w72.f
  sbyte.f
  sbytes.f
  skgb.f
  start.f
  summary.f
  w3difdat.f
  w3doxdat.f
  w3fi01.f
  w3fi58.f
  w3fi59.f
  w3fi63.f
  w3fi68.f
  w3fi71.f
  w3fi72.f
  w3fi73.f
  w3fi74.f
  w3fi75.f
  w3fi76.f
  w3fi82.f
  w3fi83.f
  w3fs21.f
  w3fs26.f
  w3kind.f
  w3locdat.f
  w3log.f
  w3movdat.f
  w3reddat.f
  w3tagb.f
  w3utcdat.f
  )

include_directories (${CMAKE_INSTALL_PREFIX}/include)

add_library (${PROJECT_NAME} ${SRCS})

INSTALL(TARGETS ${PROJECT_NAME}
        DESTINATION ${CMAKE_INSTALL_PREFIX}/lib
       )
