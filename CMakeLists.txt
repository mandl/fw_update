cmake_minimum_required (VERSION 2.8.11)

find_library(LIBUSB_LIBRARY NAME usb-1.0)

find_path(LIBUSB_INCLUDE_DIR
  NAMES libusb.h
  PATH_SUFFIXES "include" "libusb" "libusb-1.0")

find_library(LIBUSB_LIBRARY
  NAMES usb
  PATH_SUFFIXES "lib" "lib32" "lib64")


add_executable(fw_update main.cpp 
fu_usage.cpp
pic_bootloader.cpp
buffer/buffer.cpp
buffer/fragbuffer.cpp
buffer/iterator.cpp
dtrace/dtrace.cpp
exception/exception.cpp
image/argumentimage.cpp
image/binimage.cpp
image/cout_image.cpp
image/intel_hex_image.cpp
image/intel_hex_record.cpp
parser/parameter.cpp
parser/parameters.cpp
parser/parser.cpp
parser/usage.cpp
parser/usage_descriptor.cpp
parser/usage_update.cpp
 )

#target_include_directories(fw_update ${LIBUSB_INCLUDE_DIR})
target_link_libraries(fw_update ${LIBUSB_LIBRARY})



