cmake_minimum_required(VERSION 3.18)
project(RotationDetection
    VERSION 1.0.0
    DESCRIPTION "default C++ Project"
    LANGUAGES CXX
    )
add_executable(
    RotationDetection src/main.cpp
    )
set(STANDARD "C:/Developer/msys64/mingw64/include")
target_include_directories(
    RotationDetection
    PUBLIC STANDARD
 PUBLIC include
    )
add_compile_options(
  "-Wall" "-Wpedantic" "-Wextra" "-fexceptions" "-std=c++2b"
  "$<$<CONFIG:DEBUG>:-O0;-g3;-ggdb>"
)
target_link_directories(
    RotationDetection
    PUBLIC "C:/Developer/msys64/mingw64/lib"
    )
target_link_libraries(
    RotationDetection
    PUBLIC mingw32
    )
