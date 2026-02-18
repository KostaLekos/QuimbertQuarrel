cmake_minimum_required(VERSION 4.2.3)
project(Quimbert_Quarrel)

set(CMAKE_CXX_STANDARD 20)
set(CMAKE_EXPORT_COMPILE_COMMANDS on)

include_directories(include)

file(GLOB SOURCES "src/*.cpp")

add_subdirectory(dependencies/raylib)

add_executable(${PROJECT_NAME} ${SOURCES})

target_link_libraries(${PROJECT_NAME} PRIVATE raylib m pthread dl rt GL X11 Xrandr Xi GLU)