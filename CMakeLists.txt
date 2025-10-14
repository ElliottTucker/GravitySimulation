cmake_minimum_required(VERSION 3.27)
project(GravitySimulation)

set(CMAKE_CXX_STANDARD 17)

# Find GLFW
find_package(glfw3 REQUIRED)

# Add your executable (main.cpp and glad.c)
add_executable(GravitySimulation main.cpp glad.c)

# Include GLAD headers
target_include_directories(GravitySimulation PRIVATE ${CMAKE_SOURCE_DIR}/include)

# Link GLFW
target_link_libraries(GravitySimulation glfw)