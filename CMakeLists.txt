cmake_minimum_required(VERSION 3.20)
project(chip8emu)

set(CMAKE_CXX_STANDARD 20)

set(SDL2_PATH "C:\\Users\\Filip\\Downloads\\SDL2-2.0.16\\x86_64-w64-mingw32")
find_package(SDL2 REQUIRED)
include_directories( ${SDL2_INCLUDE_DIR} )

add_executable(chip8emu src/main.cpp src/chip8.cpp src/chip8.hpp src/Platform.cpp src/Platform.hpp)

target_link_libraries(chip8emu ${SDL2_LIBRARY} )


