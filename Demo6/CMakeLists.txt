# 指定运行此配置文件所需的 CMake 的最低版本
cmake_minimum_required(VERSION 3.0)
# 参数值是 Demo6，该命令表示项目的名称是 Demo6
project(Demo6)
# 将名为 main.c 的源文件编译成一个名称为 app 的可执行文件
add_executable(app main.c)


# 单个源文件
#[[
├── CMakeLists.txt
└── main.c
]]
# 第一步 执行cmake
#[[
直接在当前目录 cmake . 不好 混在一起了
[root@localhost Demo6]# tree -L 1 .
.
├── CMakeCache.txt
├── CMakeFiles
├── cmake_install.cmake
├── CMakeLists.txt
├── main.c
└── Makefile
]]
#[[
mkdir build
直接在build目录 cmake ..
[root@localhost Demo6]# tree -L 2 .
.
├── build
│   ├── CMakeCache.txt
│   ├── CMakeFiles
│   ├── cmake_install.cmake
│   └── Makefile
├── CMakeLists.txt
└── main.c
]]

# 第二步 在含有Makefile目录 make
# 第三步 运行 ./app 10 3