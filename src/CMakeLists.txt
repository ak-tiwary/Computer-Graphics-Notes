
# Search all the .cpp files in the directory where CMakeLists lies and set them to ${SOURCE_FILES}.
# Search all the .h files in the directory where CMakeLists lies and set them to ${INCLUDE_FILES}.

 file(GLOB SOURCE_FILES ${CMAKE_CURRENT_SOURCE_DIR}/*.cpp)
# file(GLOB SOURCE_FILES2 ${CMAKE_CURRENT_SOURCE_DIR}/learnopengl/getting_started/*.cpp)
# file(GLOB SOURCE_FILES3 ${CMAKE_CURRENT_SOURCE_DIR}/learnopengl/*/*.cpp)
# list (APPEND SOURCE_FILES ${SOURCE_FILES2} ${SOURCE_FILES3})

 file(GLOB INCLUDE_FILES ${CMAKE_CURRENT_SOURCE_DIR}/*.h)
# file(GLOB INCLUDE_FILES2 ${CMAKE_CURRENT_SOURCE_DIR}/learnopengl/getting_started/*.h)
# file(GLOB INCLUDE_FILES3 ${CMAKE_CURRENT_SOURCE_DIR}/learnopengl/*/*.h)
# list (APPEND INCLUDE_FILES ${INCLUDE_FILES2} ${INCLUDE_FILES3})

add_library(glad glad.c)


# Add the executable Example to be built from the source files.
 #add_executable(Example ${SOURCE_FILES} ${INCLUDE_FILES})



# Link the executable to the libraries.
#target_link_libraries(Example ${LIBRARIES})
#target_link_libraries(Example glfw)
#target_link_libraries(Example glad)
