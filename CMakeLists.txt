# Minimum CMake version required
cmake_minimum_required(VERSION 3.10)

# Project name and version
project(RISCV_IDE_Emulator VERSION 1.0 LANGUAGES CXX)

# Set C++ standard
set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED True)

# Find the Qt5 libraries
find_package(Qt5 REQUIRED COMPONENTS Widgets)

# Add the include directories for your project
include_directories(
        ${CMAKE_SOURCE_DIR}/include
)

# Add the source files for the project
set(SOURCES
        src/main.cpp
        src/gui/main_window.cpp
        src/gui/code_editor.cpp
        src/gui/console.cpp
        src/emulator/cpu.cpp
        src/emulator/memory.cpp
        src/emulator/parser.cpp
        src/emulator/instruction_set.cpp
)

# Add the header files
set(HEADERS
        include/gui/main_window.h
        include/gui/code_editor.h
        include/gui/console.h
        include/emulator/cpu.h
        include/emulator/memory.h
        include/emulator/parser.h
        include/emulator/instruction_set.h
)

# Specify the executable target
add_executable(riscv-ide ${SOURCES} ${HEADERS})

# Link the Qt5 libraries to the executable
target_link_libraries(riscv-ide Qt5::Widgets)

# Add additional compiler flags if needed
target_compile_options(riscv-ide PRIVATE -Wall -Wextra -pedantic)
