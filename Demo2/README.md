## Demo2
* mkdir build && cd build
* cmake ..
* make
* ./bin/hello
### 语法
* ADD_SUBDIRECTORY(src bin)
```
将src子目录加入工程，并指定编译输出(包含编译中间结果)路径为bin目录
如果 ADD_SUBDIRECTORY(src)
那么编译结果(包含中间结果)都将存放在build/src目录(这个目录跟原有的src目录对应)
指定bin目录后，相当于在编译时将src重名为bin,所有的中间结果和目标二进制都将存放在bin目录

EXECUTABLE_OUTPUT_PATH 重新定义目标二进制可执行文件的存放位置
SET(EXECUTABLE_OUTPUT_PATH ${PROJECT_BINARY_DIR}/bin)
ADD_SUBDIRECTORY(src)
二进制文件将放在 bin 目录下

LIBRARY_OUTPUT_PATH 重新定义目标链接库文件的存放位置
SET(LIBRARY_OUTPUT_PATH ${PROJECT_BINARY_DIR}/lib)
```
