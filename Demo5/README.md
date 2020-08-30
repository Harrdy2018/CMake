# Demo5
## 如何使用外部共享库和头文件
* ldd命令 list dynamic dependencies 列出动态依赖
* ldd build/src/main
```sh
linux-vdso.so.1 =>  (0x00007ffcd65bf000)
libhello.so.1 => not found
libc.so.6 => /lib64/libc.so.6 (0x00007ff5fbea7000)
/lib64/ld-linux-x86-64.so.2 (0x00007ff5fc274000)
```
