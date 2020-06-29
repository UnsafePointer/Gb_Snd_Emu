cmake_minimum_required(VERSION 3.10.2)
project(gb_snd_emu)

add_library(gb_snd_emu gb_apu/Blip_Buffer.cpp gb_apu/Gb_Apu.cpp gb_apu/Gb_Oscs.cpp gb_apu/Multi_Buffer.cpp)
target_include_directories(gb_snd_emu PUBLIC ./)
