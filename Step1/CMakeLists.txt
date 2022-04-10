# 指定Cmake 最低版本号
cmake_minimum_required(VERSION 3.10)

# set the project name，项目名和版本号
project(Tutorial VERSION 1.0)

# specify the C++ standard ，设置C++标准号，确保将CMAKE_CXX_STANDARD声明添加到add_executable的上面
#set(CMAKE_CXX_STANDARD 11)
#set(CMAKE_CXX_STANDARD_REQUIRED True)


# configure a header file to pass some of the CMake the settings 
# to the source code 配置一个头文件并将版本号传递给源代码：
configure_file(TutorialConfig.h.in TutorialConfig.h) 

# add the executable，构建该工程需要的文件
add_executable(Tutorial tutorial.cxx)

#因为配置的文件将被写到binary tree目录下（CMakeCache.txt所在的目录，即build目录），
#所以我们必须将那个目录添加到include搜索路径列表中。将下面这行添加到CMakeLists.txt文件的末尾：
# add the binary tree to the search path for include files 
# so that we will find TutorialConfig.h
target_include_directories(
    Tutorial PUBLIC
    "${PROJECT_BINARY_DIR}"
)