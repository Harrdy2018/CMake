cmake_minimum_required(VERSION 3.0)
project(Demo8)
# 添加 math 子目录
add_subdirectory(math)
add_executable(app main.c)
# 添加链接库
target_link_libraries(app MathFunctions)



# 多个目录多个源文件