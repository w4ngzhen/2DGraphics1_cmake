CMAKE_MINIMUM_REQUIRED(VERSION 3.22)
PROJECT(2DGraphics1_cmake)

SET(CMAKE_CXX_STANDARD 11)

# cmake子项目，子项目的名称就是子目录下的CMakeLists.txt中的PROJECT一致的名称
ADD_SUBDIRECTORY(NimotsuKunBox)
ADD_SUBDIRECTORY(drawPixels)