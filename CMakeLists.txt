cmake_minimum_required(VERSION 3.0)

project(software-renderer)

set(OpenGL_GL_PREFERENCE "GLVND")

find_package(SFML 2.5.0 COMPONENTS audio graphics network system window REQUIRED)
find_package(OpenGL REQUIRED)

add_executable(software-renderer src/main.cpp)

target_link_libraries(software-renderer PUBLIC 
                      sfml-audio
                      sfml-system
                      sfml-graphics
                      sfml-network 
                      sfml-window 
                      OpenGL::GL)