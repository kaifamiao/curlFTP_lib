cmake_minimum_required(VERSION 3.24)
project(curlFTP_lib C)

set(CMAKE_C_STANDARD 11)
set(PROJECT_NAME curlFTP_lib)


set(LIB_PATH1 D:\\curl)

set(PROJECT_INCLUDE ${LIB_PATH1})
set(PROJECT_LIB ${LIB_PATH1})


add_library(${PROJECT_NAME} library.c)
##include_directories(.)  #这个也可以放在add_executable前面
# 设置头文件路径 这里设置为 [当前目录/include]
include_directories(${PROJECT_NAME}
        PRIVATE
        ${PROJECT_INCLUDE}/include
        #        ${PROJECT_SOURCE_DIR}/include
        )
target_link_libraries(${PROJECT_NAME}
        PRIVATE
#        ${PROJECT_LIB}/lib/libcurl.dll.a
        )


