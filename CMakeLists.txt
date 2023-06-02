cmake_minimum_required(VERSION 3.16.0)
project(VulkanFrame)
set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

add_subdirectory(external/glfw)
add_subdirectory(external/imgui_cmake)

include_directories(
    include
)

add_library(VulkanFrame STATIC
    src/Layer.cpp
    src/Application.cpp
)

target_link_libraries(VulkanFrame
    ImGui
)