add_definitions(-DQAPPLICATION_CLASS=QApplication)
add_library(SingleApplication STATIC singleapplication.cpp singleapplication.h singleapplication_p.h)
target_link_libraries(SingleApplication Qt5::Core Qt5::Network Qt5::Widgets)
target_include_directories(SingleApplication INTERFACE ${CMAKE_CURRENT_SOURCE_DIR})
