# 指定运行此配置文件所需的 CMake 的最低版本
#cmake_minimum_required(VERSION 3.0)
# 参数值是 Demo7，该命令表示项目的名称是 Demo7
#project(Demo7)
# 将名为 main.c MathFunctions.c 的源文件编译成一个名称为 app 的可执行文件
#add_executable(app main.c MathFunctions.c)


# 也可以这样
cmake_minimum_required(VERSION 3.0)
project(Demo7)
# 查找当前目录下的所有源文件
# 并将名称保存到 mySourceFiles 变量
aux_source_directory(. mySourceFiles)
message(STATUS "test 1 " ${mySourceFiles})
add_executable(app ${mySourceFiles})




# 同一目录多个源文件