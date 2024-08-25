cmake_minimum_required(VERSION 3.30)

# Set compilers and other tools
set(CMAKE_C_COMPILER "C:/Program Files/Microsoft Visual Studio/2022/Community/VC/Tools/MSVC/14.41.34120/bin/Hostx64/x64/cl.exe")
set(CMAKE_CXX_COMPILER "C:/Program Files/Microsoft Visual Studio/2022/Community/VC/Tools/MSVC/14.41.34120/bin/Hostx64/x64/cl.exe")
set(CMAKE_MT "C:/Program Files (x86)/Windows Kits/10/bin/10.0.22621.0/x64/mt.exe")
set(CMAKE_RC_COMPILER "C:/Program Files (x86)/Windows Kits/10/bin/10.0.22621.0/x64/rc.exe")

set(PROJECT_NAME helloWorld)
project(${PROJECT_NAME})

include($ENV{DEVKIT_LOCATION}/cmake/pluginEntry.cmake)

set(SOURCE_FILES
    helloWorld.cpp
)

set(LIBRARIES
    OpenMaya Foundation
)

build_plugin()