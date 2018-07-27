cmake_minimum_required(VERSION 3.12)
project(opengl_tutorial_cpp)

find_package(OpenGL REQUIRED)

set(CMAKE_CXX_STANDARD 14)

include_directories(
        C:/glew-2.1.0/include
        C:/glfw-3.1.1.bin.WIN64/include
        C:/glm-0.9.9.0
)
link_directories(
        C:/glew-2.1.0/lib/Release/x64
        C:/glfw-3.1.1.bin.WIN64/lib-vc2013
)

set(ALL_LIBS
        ${OPENGL_LIBRARY}
        glew32
        glfw3
        )

add_executable(opengl_tutorial_cpp main.cpp)

target_link_libraries(opengl_tutorial_cpp
        ${ALL_LIBS}
        )
