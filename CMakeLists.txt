cmake_minimum_required(VERSION 3.2)
project(SingleApplication)
set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_AUTOMOC ON)
add_library(SingleApplication STATIC singleapplication.cpp singleapplication.h singleapplication_p.h)
target_link_libraries(SingleApplication Qt5::Core Qt5::Network Qt5::Widgets)
target_compile_definitions(SingleApplication PUBLIC -DQAPPLICATION_CLASS=QApplication)
target_include_directories(SingleApplication INTERFACE ${CMAKE_CURRENT_SOURCE_DIR})
