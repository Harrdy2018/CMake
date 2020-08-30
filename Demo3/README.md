## Demo3
* mkdir build && cd build
* cmake -DCMAKE_INSTALL_PREFIX=/home/harrdy/Desktop/test ..
* make
* make install
```
[root@localhost build]# cmake  -DCMAKE_INSTALL_PREFIX=/home/harrdy/Desktop/test ..
-- The C compiler identification is GNU 4.8.5
-- Detecting C compiler ABI info
-- Detecting C compiler ABI info - done
-- Check for working C compiler: /usr/bin/cc - skipped
-- Detecting C compile features
-- Detecting C compile features - done
-- Configuring done
-- Generating done
-- Build files have been written to: /home/harrdy/Desktop/CMake/Demo3/build
[root@localhost build]# make
Scanning dependencies of target hello
[ 50%] Building C object bin/CMakeFiles/hello.dir/main.c.o
[100%] Linking C executable hello
[100%] Built target hello
[root@localhost build]# make install
[100%] Built target hello
Install the project...
-- Install configuration: ""
-- Installing: /home/harrdy/Desktop/test/share/doc/cmake/t2/COPYRIGHT
-- Installing: /home/harrdy/Desktop/test/share/doc/cmake/t2/README
-- Installing: /home/harrdy/Desktop/test/bin/runhello.sh
-- Installing: /home/harrdy/Desktop/test/share/doc/camke/t2
-- Installing: /home/harrdy/Desktop/test/share/doc/camke/t2/hello.txt
```
### 如果没有定义 -DCMAKE_INSTALL_PREFIX
* 默认定义是 /usr/local
```sh
Install the project...
-- Install configuration: ""
-- Installing: /usr/local/share/doc/cmake/t2/COPYRIGHT
-- Installing: /usr/local/share/doc/cmake/t2/README
-- Installing: /usr/local/bin/runhello.sh
-- Installing: /usr/local/share/doc/camke/t2
-- Installing: /usr/local/share/doc/camke/t2/hello.txt
```
