# RISC-V Assembler IDE and Emulator

## Overview

This project is a desktop application for Arch Linux, providing an integrated development environment (IDE) for writing, executing, and debugging RISC-V assembler code. It includes a built-in RISC-V processor emulator, a code editor with syntax highlighting, and a console for input/output operations.

## Features

- **RISC-V Emulator**: A custom-built RISC-V CPU emulator that supports the RV32I instruction set.
- **Assembler Code Editor**: A code editor with RISC-V syntax highlighting and autocompletion.
- **Execution and Debugging**: Step-by-step execution of assembler programs, including setting breakpoints and inspecting registers and memory.
- **Input/Output Console**: A console for interacting with the running program, simulating syscalls like `ecall` for input and output operations.

## Requirements

To build and run this project, you will need the following dependencies:

- **CMake**: Build system to compile the project.
- **Qt5**: For the graphical user interface (GUI).
- **GCC/G++**: C++ compiler for compiling the emulator and application code.
- **Flex/Bison** (optional): If you want to use them for parsing assembler code.
  
Install dependencies on Arch Linux:

```bash
sudo pacman -S cmake qt5-base gcc
