# Project README

## Overview
This project is a basic implementation of an Excel-like application in C. It provides a graphical interface for displaying and manipulating data, similar to Microsoft Excel.

## Features
- Basic cell manipulation and display.
- Support for custom functions defined in a script file.
- Cross-platform compilation (Linux, Windows, Wine, WebAssembly).

## Project Structure

### Prerequisites
- GCC compiler
- Make utility
- Standard development tools
- Libraries needed:
  - X11 library for Linux GUI
  - user32, gdi32, winmm libraries for Windows and Wine

## Build & Run

### Building for Linux
To build the project on a Linux system, execute the following steps:
```bash
cd /path/to/project
make -f Makefile.linux all
```
This will compile the source code into an executable located in the `build` directory.

### Running on Linux
After building, you can run the application using:
```bash
./build/Main
```

### Building for Windows
For a Windows build, use:
```bash
cd /path/to/project
make -f Makefile.windows all
```
This will compile the source code into an executable `Main.exe` located in the `build` directory.

### Running on Windows
Run the compiled executable:
```cmd
./build/Main.exe
```

### Building for Wine
To build the project using Wine, execute:
```bash
cd /path/to/project
make -f Makefile.wine all
```
Then run the application:
```bash
WINEPREFIX=~/wine64 WINEARCH=win64 wine ./build/Main.exe
```

### Building for WebAssembly (Emscripten)
For a web build, use:
```bash
cd /path/to/project
make -f Makefile.web all
```
This will compile the source code into an HTML file located in the `build` directory. You can serve this file using any web server to view it in a browser.

### Build Options
- `make -f Makefile.(os) all`: Builds the project.
- `make -f Makefile.(os) do`: Builds and runs the project.
- `make -f Makefile.(os) clean`: Cleans the build artifacts.
- `make -f Makefile.(os) exe`: Runs the built executable.

Each directory and file is present in the Project Organization as specified. The code for the main application is located in `src/Main.c`.