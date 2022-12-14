# This CMakeLists is intended only for macOS and Linux.

cmake_minimum_required(VERSION 3.1)

# Set a project name.
project(HelloOpenGL)

 # CMake 2.8.12 or newer


# Use the C++17 standard.


#set(CMAKE_FIND_DEBUG_MODE 0)
set(CMAKE_EXPORT_COMPILE_COMMANDS ON)
# Suppress warnings of the deprecation of glut functions on macOS.
add_definitions(-Wno-deprecated-declarations)




# Find the packages we need.
find_package(OpenGL REQUIRED)
find_package(GLUT REQUIRED)
find_package(glfw3 3.3 REQUIRED)

find_package(OpenCV 4 REQUIRED)







# OPENGL_INCLUDE_DIR, GLUT_INCLUDE_DIR, OPENGL_LIBRARIES, and GLUT_LIBRARIES
# are CMake built-in variables defined when the packages are found.

set(INCLUDE_DIRS ${OPENGL_INCLUDE_DIR} ${GLUT_INCLUDE_DIR} ${GLEW_INCLUDE_DIR})
set(LIBRARIES ${OPENGL_LIBRARIES} ${GLUT_LIBRARIES} ${GLEW_LIBRARIES})
set( CMAKE_RUNTIME_OUTPUT_DIRECTORY ${PROJECT_SOURCE_DIR}/build )
set(CMAKE_EXE_LINKER_FLAGS "${CMAKE_EXE_LINKER_FLAGS} -framework Cocoa -framework OpenGL -framework IOKit -framework CoreFoundation -framework CoreVideo")


include_directories(${INCLUDE_DIRS})
include_directories(/usr/local/include)
include_directories(${PROJECT_SOURCE_DIR}/dependencies/include)

# Add the list of include paths to be used to search for include files.


add_subdirectory(${PROJECT_SOURCE_DIR}/src)
add_subdirectory(${PROJECT_SOURCE_DIR}/src/learnopengl)
