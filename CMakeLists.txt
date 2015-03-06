cmake_minimum_required(VERSION 2.8)
project(TestGtk)
set(EXECUTABLE_OUTPUT_PATH bin/${CMAKE_BUILD_TYPE})
find_package(GTK2 REQUIRED)
include_directories(${GTK2_INCLUDE_DIRS})
add_executable(
	test-gtk
	src/main.c
	)
target_link_libraries(
	test-gtk
	${GTK2_LIBRARIES}
	)
