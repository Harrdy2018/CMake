## Demo1
### 语法
* PROJECT(HELLO C)
```
定义工程名称为HELLO 指定工程支持的语言为C语言
这个指令隐式的定义了两个CMake变量
MESSAGE(STATUS "test 1 " ${PROJECT_BINARY_DIR})
MESSAGE(STATUS "test 2 " ${PROJECT_SOURCE_DIR})
同理
MESSAGE(STATUS "test 3 " ${HELLO_BINARY_DIR})
MESSAGE(STATUS "test 4 " ${HELLO_SOURCE_DIR})
```
* SET(NAME Harrdy) 新建变量
```
定义多个源文件列表
SET(SRC_LIST main.c t1.c t2.c)
```
* MESSAGE(STATUS "test 6 " ${NAME})
```
MESSAGE(STATUS "test 6 " ${NAME})  信息前面带'-'
MESSAGE(SEND_ERROR "test 6 " ${NAME})  产生错误，生成过程被跳过
MESSAGE(FATAL_ERROR "test 6 " ${NAME})  立即终止所有cmake过程
```
* ADD_EXECUTABLE(hello ${SRC_LIST})
```
定义了这个工程会生成一个名为hello的可执行文件，
相关的源文件是 SRC_LIST 中定义的源文件列表
本例中等价于 ADD_EXECUTABLE(hello main.c)
```
### 内部构建(in-source build) 直接在工程目录下构建
* cmake .
* make 如果想要获取详细信息 make VERBOSE=1
* make clean 对构建结果进行清理
* ./hello
### 外部构建(out-of-source build) 直接在build目录下构建
* mkdir build && cd build
* cmake ..
* make VERBOSE=1
* ./hello
### 区别
* 内部构建不会产生build目录，产生的中间文件混在了一起很烦,外部构建全在build文件
* 变量不一样
```
内部构建 
MESSAGE(STATUS "test 1 " ${PROJECT_BINARY_DIR}) hello最终在工程目录下
MESSAGE(STATUS "test 2 " ${PROJECT_SOURCE_DIR}) 工程目录
外部构建 
MESSAGE(STATUS "test 1 " ${PROJECT_BINARY_DIR}) hello最终在build目录下
MESSAGE(STATUS "test 2 " ${PROJECT_SOURCE_DIR}) 工程目录
```
