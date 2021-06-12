cmake_minimum_required(VERSION 3.19)
set(CMAKE_PREFIX_PATH  "E:\\Qt\\5.15.2\\mingw81_64")
project(Barybians_API_library)
find_package( Qt5Core REQUIRED)
find_package( Qt5Widgets REQUIRED)
find_package( Qt5Gui REQUIRED )
find_package( Qt5Network REQUIRED )
find_package( Qt5OpenGL REQUIRED )
set(CMAKE_CXX_STANDARD 11)

add_library(Barybians_API_library webconnector.cpp webconnector.h Data.cpp Data.h)

target_link_libraries(Barybians_API_library PRIVATE Qt${QT_VERSION_MAJOR}::Widgets)
target_link_libraries(Barybians_API_library PRIVATE Qt${QT_VERSION_MAJOR}::Network)

