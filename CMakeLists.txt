cmake_minimum_required(VERSION 3.10.2)
project(gb_snd_emu)

find_package(SDL2 REQUIRED)
include_directories(${SDL2_INCLUDE_DIRS})

add_library(gb_snd_emu gb_apu/Blip_Buffer.cpp gb_apu/Gb_Apu.cpp gb_apu/Gb_Oscs.cpp gb_apu/Multi_Buffer.cpp gb_apu/Sound_Queue.cpp)
target_include_directories(gb_snd_emu PUBLIC ./)

target_link_libraries(gb_snd_emu ${SDL2_LIBRARIES})
