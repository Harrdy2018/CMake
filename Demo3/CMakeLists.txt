cmake_minimum_required(VERSION 3.0)
PROJECT(HELLO C)
ADD_SUBDIRECTORY(src bin)

#安装 COPYRIGHT/README
INSTALL(FILES COPYRIGHT README DESTINATION share/doc/cmake/t2)
#安装 runhello.sh
INSTALL(PROGRAMS runhello.sh DESTINATION bin)
#安装 doc/hello.txt
INSTALL(DIRECTORY doc/ DESTINATION share/doc/camke/t2)
