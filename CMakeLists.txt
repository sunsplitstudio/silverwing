cmake_minimum_required(VERSION 3.25)
project(MySDL3App VERSION 1.0 LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

# Add SDL submodule
add_subdirectory(externals/SDL)

# Create executable
add_executable(MySDL3App src/main.cpp)

# Link SDL3 libraries
target_link_libraries(MySDL3App PRIVATE SDL3::SDL3)
