cmake_minimum_required(VERSION 3.16)

project(mikeGL VERSION 0.1)

add_subdirectory(libs)

add_executable(mikeGL mikeGL.cpp)

target_link_libraries(mikeGL PUBLIC glad "/usr/lib/x86_64-linux-gnu/libglfw.so.3.3" "/lib/x86_64-linux-gnu/libdl.so.2")

target_include_directories(mikeGL PUBLIC
                           "${PROJECT_SOURCE_DIR}/include/"
                           "/usr/include/GLFW")

# message("${PROJECT_SOURCE_DIR}/include")