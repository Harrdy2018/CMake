# Demo4
## 静态库与动态库构建
```
建立一个静态库和动态库，提供HelloFunc函数供其他程序编程使用，
HelloFunc向终端输出Hello World 字符串
```
### 语法
* ADD_LIBRARY(hello SHARED ${LIBHELLO_SRC})
```
hello 系统自动生成 libhello.X
SHARED 动态库
STATIC 静态库
```
### 安装共享库和头文件
* mkdir build && cd build
* cmake -DCMAKE_INSTALL_PREFIX=/usr ..
* make
* make install
```
[ 50%] Built target hello
[100%] Built target hello_static
Install the project...
-- Install configuration: ""
-- Installing: /usr/lib/libhello.so.1.2
-- Installing: /usr/lib/libhello.so.1
-- Installing: /usr/lib/libhello.so
-- Installing: /usr/lib/libhello.a
-- Installing: /usr/include/hello/hello.h
```
