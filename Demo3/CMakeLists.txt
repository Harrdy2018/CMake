cmake_minimum_required(VERSION 3.0)
PROJECT(HELLO C)
ADD_SUBDIRECTORY(src bin)

#普通文件安装 COPYRIGHT/README
INSTALL(FILES COPYRIGHT README DESTINATION share/doc/cmake/t2)
#非目标文件的可执行程序安装(比如脚本之类) runhello.sh
INSTALL(PROGRAMS runhello.sh DESTINATION bin)
#目录安装 doc/hello.txt
INSTALL(DIRECTORY doc/ DESTINATION share/doc/camke/t2)
