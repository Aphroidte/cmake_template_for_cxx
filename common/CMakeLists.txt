# 添加源文件
## 添加 .cpp 文件
message("common: ${PROJECT_SOURCE_DIR}")
aux_source_directory(${PROJECT_SOURCE_DIR}/common COMMON_SRC_DIR)

# 设置库文件的输出路径
set(LIBRARY_OUTPUT_PATH ${PROJECT_SOURCE_DIR}/common/)

# 编译静态库
add_library("common" STATIC ${COMMON_SRC_DIR})
