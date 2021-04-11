# CMakeLists for AparData library

project (w3)

set (SRCS
  getgb.f
  getgbmh.f
  putgbex.f
  w3fi73.f
  getgb1r.f
  getgbmp.f
  putgbn.f
  w3fi74.f
  getgb1re.f
  getgbp.f
  r63w72.f
  w3fi75.f
  getgb1s.f
  getgi.f
  sbyte.f
  w3fi76.f
  getgbe.f
  getgir.f
  sbytes.f
  w3fi82.f
  getgbeh.f
  idsdef.f
  skgb.f
  w3fi83.f
  getgbem.f
  iw3jdn.f
  w3difdat.f
  w3fs26.f
  getgbemh.f
  ixgb.f
  w3doxdat.f
  w3log.f
  getgbemp.f
  lengds.f
  w3fi01.f
  w3movdat.f
  getgbens.f
  pdsens.f
  w3fi58.f
  w3reddat.f
  getgbep.f
  pdseup.f
  w3fi59.f
  w3tagb.f
  errmsg.f
  getgbex.f
  putgb.f
  w3fi63.f
  getgbexm.f
  putgbe.f
  w3fi68.f
  baciof.f
  gbytes_char.f
  getgbh.f
  putgben.f
  w3fi71.f
  gbyte.f
  getbit.f
  getgbm.f
  putgbens.f
  errexit.f
  fparsei.f
  fparser.f
  instrument.f
  start.f
  summary.f
  w3utcdat.f
  w3fs21.f
  w3locdat.f
  )

add_library (${PROJECT_NAME} STATIC ${SRCS})
set_target_properties(${PROJECT_NAME} PROPERTIES LINKER_LANGUAGE C)

INSTALL(TARGETS ${PROJECT_NAME}
        DESTINATION ${CMAKE_INSTALL_PREFIX}/lib
       )
