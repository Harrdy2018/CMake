SET(LIBHELLO_SRC hello.c)

# 动态库
ADD_LIBRARY(hello SHARED ${LIBHELLO_SRC})
# 动态库版本号
# VERSION 动态库版本
# SOVERSION API 版本
SET_TARGET_PROPERTIES(hello PROPERTIES VERSION 1.2 SOVERSION 1)

# 静态库
ADD_LIBRARY(hello_static STATIC ${LIBHELLO_SRC})
SET_TARGET_PROPERTIES(hello_static PROPERTIES OUTPUT_NAME "hello")
GET_TARGET_PROPERTY(OUTPUT_VALUE hello_static OUTPUT_NAME)
MESSAGE(STATUS "test 1 " ${OUTPUT_VALUE})

# 安装共享库 静态库要使用 ARCHIVE关键字
# linux 共享库目录 /usr/lib
INSTALL(TARGETS hello hello_static
        LIBRARY DESTINATION lib
        ARCHIVE DESTINATION lib)
# 安装头文件
# linux 头文件目录 /usr/include
INSTALL(FILES hello.h DESTINATION include/hello)
