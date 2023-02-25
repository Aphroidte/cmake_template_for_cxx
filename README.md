# cmake_template_for_cxx
使用 cmake 进行构建与调试 C++ 程序的模板

## 单元测试

1. 创建一个用于存放单元测试代码以及 GTest 框架的源码。
2. 编译 GTest 的源码：进入 googletest 目录，执行 cmake 

> git clone https://github.com/google/googletest.git -b release-1.10.0
>
> 或者在 https://github.com/google/googletest/releases 中下载最新的源码

如果 windows 执行 cmake 编译时报错：set_target_properties 语法错误；大概率是因为没有声明 GOOGLETEST_VERSION 变量导致的；在 cmake 文件开头添加语句：set(GOOGLETEST_VERSION 这里填写你下载的gtest版本)；比如set(GOOGLETEST_VERSION 1.11.0)

> 注意：Gtest 使用 1.13.0 版本的话，需要使用 C++14 以上进行编译。
