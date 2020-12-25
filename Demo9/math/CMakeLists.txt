aux_source_directory(. mySourceFiles)
message(STATUS "test inner " ${mySourceFiles})
# 生成链接库 add_library 将 math 目录中的源文件编译为静态链接库
add_library(MathFunctions ${mySourceFiles})