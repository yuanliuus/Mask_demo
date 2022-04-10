# CMake file for making GDS files using libmask. Created by Yuan Liu on 02/17/2017
# Normally you only need to use .cpp files for your source file and change the varibles below accordingly.


cmake_minimum_required(VERSION 3.6)


# Change the information below accordingly.

set(GDS_FILENAME "mask_example.gds")
set(MASK_NAME "mask_example")

set(PDK_NAME "pdk_demo")
set(PDK_VERSION "0.2")

# "[PDK NAME]/[PDK VERSION]@[FOUNDRY NAME]/[REVISION]"
set(PDK_REQUIRED "pdk_demo/0.2@cmalips/stable")

################

# DO NOT modifiy codes below
message(STATUS "Downloading mask.cmake ...")
file(DOWNLOAD "https://raw.githubusercontent.com/yuanliuus/MaskFiles/master/mask.cmake"
         "${CMAKE_BINARY_DIR}/mask.cmake")
include(${CMAKE_BINARY_DIR}/mask.cmake)

