cmake_minimum_required(VERSION 2.8.6)
project(practice_tutorial_pendulum)
add_compile_options(-std=gnu++11)
add_compile_options(-Wdeprecated-declarations)

find_package(Eigen3 REQUIRED)
find_package(OpenGL REQUIRED)
find_package(GLUT REQUIRED)
find_package(DART REQUIRED COMPONENTS utils-urdf gui CONFIG)
include_directories(${EIGEN3_INCLUDE_DIR})
include_directories(${DART_INCLUDE_DIRS})

file(GLOB srcs "*.h" "*.cpp")

add_executable(practice_tutorial_pendulum ${srcs})
target_link_libraries(practice_tutorial_pendulum ${DART_LIBRARIES})