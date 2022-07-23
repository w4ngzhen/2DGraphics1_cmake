CMAKE_MINIMUM_REQUIRED(VERSION 3.22)
PROJECT(NimotsuKunBox)

SET(CMAKE_CXX_STANDARD 11)

# 配置编译器以指定编码读取代码源文件
ADD_COMPILE_OPTIONS("$<$<C_COMPILER_ID:MSVC>:/utf-8>")
ADD_COMPILE_OPTIONS("$<$<CXX_COMPILER_ID:MSVC>:/utf-8>")

MESSAGE("Current CMakeLists.txt dir:\n${CMAKE_CURRENT_SOURCE_DIR}")

# 配置头文件查找路径
INCLUDE_DIRECTORIES(${CMAKE_CURRENT_SOURCE_DIR}/../@lib/include)
# 配置链接库文件查找路径
LINK_DIRECTORIES(${CMAKE_CURRENT_SOURCE_DIR}/../@lib/lib)

ADD_EXECUTABLE(NimotsuKunBox main.cpp)

# 实际链接
TARGET_LINK_LIBRARIES(NimotsuKunBox GameLib_d.lib)