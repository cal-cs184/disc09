# Original file Copyright CMU462 Fall 2015: 
# Kayvon Fatahalian, Keenan Crane,
# Sky Gao, Bryce Summers, Michael Choquette.
link_libraries(CGL)

include_directories("${PROJECT_SOURCE_DIR}/include")

link_libraries(
  glfw ${GLFW_LIBRARIES}
  glew ${GLEW_LIBRARIES}
  ${OPENGL_LIBRARIES}
  ${FREETYPE_LIBRARIES}
)

add_executable(triangle triangle.cpp)
add_executable(text text.cpp)
add_executable(event event.cpp)
add_executable(template template.cpp)

# Install examples
install(TARGETS triangle DESTINATION bin/examples)