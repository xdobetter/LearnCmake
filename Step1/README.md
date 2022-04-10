# Introduction
关于cmake的学习

# 什么是Cmake
一句计算机名言，通过添加中间层，可以解决计算机中的所有问题。
> All problems in computer science can be solved by another level of indirection.
> David Wheeler'

你或许听过好几种 Make 工具，例如 GNU Make ，QT 的 qmake ，微软的 MS nmake，BSD Make（pmake），Makepp，等等。这些 Make 工具遵循着不同的规范和标准，所执行的 Makefile 格式也千差万别。这样就带来了一个严峻的问题：如果软件想跨平台，必须要保证能够在不同平台编译。而如果使用上面的 Make 工具，就得为每一种标准写一次 Makefile ，这将是一件让人抓狂的工作。

CMake就是针对上面问题所设计的工具：它首先允许开发者编写一种平台无关的 CMakeList.txt 文件来定制整个编译流程，然后再根据目标用户的平台进一步生成所需的本地化 Makefile 和工程文件，如 Unix 的 Makefile 或 Windows 的 Visual Studio 工程。从而做到“Write once, run everywhere”。显然，CMake 是一个比上述几种 make 更高级的编译配置工具。一些使用 CMake 作为项目架构系统的知名开源项目有 VTK、ITK、KDE、OpenCV、OSG 等

# cmake 构建Pipeline


# Hint

1.在windows下，编译出的ZERO_CHECK和ALL_BUILD是个什么东西呢？

# Ref

[cmake教程官网](https://cmake.org/cmake/help/v3.17/guide/tutorial/index.html#adding-system-introspection-step-5)
[CMake教程（一）](https://zhuanlan.zhihu.com/p/119426899)
[CMake官方教程](https://blog.csdn.net/weixin_43669941/article/details/112913301)
> 对官方教程的一个翻译，很不错的一个教程