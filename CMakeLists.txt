cmake_minimum_required(VERSION 3.26)
project(Trees)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_BUILD_TYPE Debug)

set(EXTERNAL_LIBRARIES_INCLUDE_DIRS "")
set(EXTERNAL_LIBRARIES "")

set(Qt5_DIR "/opt/homebrew/Cellar/qt@5/5.15.10/lib/cmake/Qt5")
find_package(Qt5 REQUIRED COMPONENTS Core Widgets Gui) 
list(APPEND EXTERNAL_LIBRARIES_INCLUDE_DIRS ${Qt5Core_INCLUDE_DIRS} ${Qt5Widgets_INCLUDE_DIRS} ${Qt5Gui_INCLUDE_DIRS})
list(APPEND EXTERNAL_LIBRARIES ${Qt5Core_LIBRARIES} ${Qt5Widgets_LIBRARIES} ${Qt5Gui_LIBRARIES})
include_directories(
    ${CMAKE_CURRENT_SOURCE_DIR}
    ${EXTERNAL_LIBRARIES_INCLUDE_DIRS}
)

add_executable(test main.cpp mainwindow.cpp node.cpp tree.cpp Vertex.cpp)
target_link_libraries(test ${EXTERNAL_LIBRARIES})