cmake_minimum_required (VERSION 2.8.9)
project (lighting-test)
find_package (Qt5 COMPONENTS Core Gui Widgets OpenGL)
# Find the QtWidgets library
set(QT_USE_QTOPENGL TRUE)
set (CMAKE_CXX_FLAGS "-Wall -std=c++11 -ggdb -pg")

include_directories (${Qt5Widgets_INCLUDE_DIRS} ${lighting-test_SOURCE_DIR}/src)
set (EXECUTABLE_OUTPUT_PATH "${lighting-test_BINARY_DIR}/bin")

add_subdirectory (src)