project(libptp2)
cmake_minimum_required(VERSION 3.18)

#TODO add cmakemodule to find lib usb

add_library(ptp2 src/ptp.c src/properties.c src/myusb.c)

add_executable(ptpcam src/ptpcam.c)
target_link_libraries(ptpcam ptp2 usb)