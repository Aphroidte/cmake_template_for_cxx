set(THIS_PROJECT_NAME main)
# 声明头文件路径以及需要链接的静态库/动态库的路径
## 头文件

## 静态库

## 包含需要用到的子项目（子项目都被链接成静态库来使用）
include_directories(${PROJECT_SOURCE_DIR}/common/)
link_directories(${PROJECT_SOURCE_DIR}/common/)
#add_subdirectory(${PROJECT_SOURCE_DIR}/common/ ${PROJECT_SOURCE_DIR}/common/)

# 引入需要编译的文件，声明需要编译目标
aux_source_directory(./ SRC_MAIN_DIR)

## 编译成可执行文件
add_executable(${THIS_PROJECT_NAME} ${SRC_MAIN_DIR})

#---------------------------------------------------------------------
## 链接静态库/动态库
target_link_libraries(${THIS_PROJECT_NAME} PUBLIC -lcommon)
