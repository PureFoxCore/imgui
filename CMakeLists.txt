cmake_minimum_required(VERSION 3.8)

project(imgui)
file(GLOB_RECURSE imguiFiles    ${CMAKE_SOURCE_DIR}/${PROJECT_NAME}/imconfig.h
                                ${CMAKE_SOURCE_DIR}/${PROJECT_NAME}/imgui.h
                                ${CMAKE_SOURCE_DIR}/${PROJECT_NAME}/imgui.cpp
                                ${CMAKE_SOURCE_DIR}/${PROJECT_NAME}/imgui_draw.cpp
                                ${CMAKE_SOURCE_DIR}/${PROJECT_NAME}/imgui_internal.h
                                ${CMAKE_SOURCE_DIR}/${PROJECT_NAME}/imgui_widgets.cpp
                                ${CMAKE_SOURCE_DIR}/${PROJECT_NAME}/imstb_rectpack.h
                                ${CMAKE_SOURCE_DIR}/${PROJECT_NAME}/imstb_textedit.h
                                ${CMAKE_SOURCE_DIR}/${PROJECT_NAME}/imstb_truetype.h
                                ${CMAKE_SOURCE_DIR}/${PROJECT_NAME}/imgui_demo.cpp)

add_library(${PROJECT_NAME} SHARED ${imguiFiles})

target_include_directories(${PROJECT_NAME} PRIVATE ${CMAKE_SOURCE_DIR}/${PROJECT_NAME}/include)