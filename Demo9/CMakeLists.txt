cmake_minimum_required(VERSION 3.0)
project(Demo9)
message(STATUS "test 1 " ${PROJECT_SOURCE_DIR}) # /home/harrdy/Desktop/CMake/Demo9
message(STATUS "test 2 " ${PROJECT_BINARY_DIR}) # /home/harrdy/Desktop/CMake/Demo9/build
add_library(myhello STATIC hello.c)
add_executable(app main.c)
# 添加链接库
target_link_libraries(app myhello)




# 创建链接库
# make 之后 build 目录就会出现 libmyhello.a

#[[
add_library(<name> [STATIC | SHARED | MODULE]
            [EXCLUDE_FROM_ALL]
            [source1] [source2 ...])
name 创建的链接库的名称，在项目中必须是全局唯一的
STATIC、SHARED或MODULE可以指定要创建的库的类型。 STATIC代表静态链接库
                                                SHARED代表动态链接库
                                                MODULE库是未链接到其他目标的插件
EXCLUDE_FROM_ALL如果给出，将在创建的目标上设置相应的属性
source 创建链接库所依赖的源文件
]]