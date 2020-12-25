cmake_minimum_required(VERSION 3.0)
project(Demo9)

message(STATUS "test 1 " ${PROJECT_SOURCE_DIR}) # /home/harrdy/Desktop/CMake/Demo9
message(STATUS "test 2 " ${PROJECT_BINARY_DIR}) # /home/harrdy/Desktop/CMake/Demo9

option(useMyMath "Use provided math implementaion" ON)

if(useMyMath)
include_directories("${PROJECT_SOURCE_DIR}/math")
#add_subdirectory(math)
set()

#add_executable(app main.c)
# 添加链接库
#target_link_libraries(app MathFunctions)



# 自定义编译选项