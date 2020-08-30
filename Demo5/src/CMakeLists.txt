ADD_EXECUTABLE(main main.c)
INCLUDE_DIRECTORIES(/usr/include/hello)
LINK_DIRECTORIES(/usr/lib)
# 给target main 添加需要链接的共享库 libhello.so
# TARGET_LINK_LIBRARIES(main libhello.so)

# 链接静态库
TARGET_LINK_LIBRARIES(main libhello.a)
