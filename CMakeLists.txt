cmake_minimum_required(VERSION 3.8)

project(imgui)
file(GLOB imguiFiles ${CMAKE_SOURCE_DIR}/${PROJECT_NAME}/*.h, ${CMAKE_SOURCE_DIR}/${PROJECT_NAME}/*.cpp)

add_library(${PROJECT_NAME} SHARED ${imguiFiles})