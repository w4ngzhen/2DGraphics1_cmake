CMAKE_MINIMUM_REQUIRED(VERSION 3.22)
PROJECT(NimotsuKunBox)

SET(CMAKE_CXX_STANDARD 11)

MESSAGE("Current CMakeLists.txt dir:\n${CMAKE_CURRENT_SOURCE_DIR}")

# 配置头文件查找路径
INCLUDE_DIRECTORIES(${CMAKE_CURRENT_SOURCE_DIR}/../@lib/include)
# 配置链接库文件查找路径
LINK_DIRECTORIES(${CMAKE_CURRENT_SOURCE_DIR}/../@lib/lib)

ADD_EXECUTABLE(NimotsuKunBox main.cpp)

# 实际链接
TARGET_LINK_LIBRARIES(NimotsuKunBox GameLib_d.lib)