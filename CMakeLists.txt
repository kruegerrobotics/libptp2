project(libptp2)
cmake_minimum_required(VERSION 3.18)

#TODO add cmakemodule to find lib usb

set(HEADERS src/ptp.h)

#option(BUILD_SHARED_LIBS "Build using shared libraries" ON)

#build the basic library
#add_library(ptp2 STATIC src/ptp.c src/properties.c src/myusb.c)
add_library(ptp2 STATIC ${HEADERS} src/ptp.c src/properties.c src/myusb.c)


#build ptpcam
add_executable(ptpcam src/ptpcam.c)
target_link_libraries(ptpcam ptp2 usb)

#installation
install(TARGETS ptp2 DESTINATION lib)
install(TARGETS ptpcam DESTINATION bin)
install(FILES ${HEADERS} DESTINATION include)