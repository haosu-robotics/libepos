remake_find_package(tulibs CONFIG)
remake_find_package(libcan CONFIG)
remake_find_library(m math.h PACKAGE libm)

remake_include(${TULIBS_INCLUDE_DIRS} ${LIBCAN_INCLUDE_DIRS})
remake_add_directories(lib)
remake_add_directories(bin COMPONENT utils)
remake_pkg_config_generate(REQUIRES tulibs libcan)
