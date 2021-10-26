# ./CMakeLists.txt，工程总配置文件

# 最低版本要求，必须
cmake_minimum_required(VERSION 3.0)

# 工程名称，这里用soTest这个名字
project(soTest)

# 添加include目录，本例头文件在./目录下，所以直接取${PROJECT_SOURCE_DIR}/
include_directories(${PROJECT_SOURCE_DIR}/src/so1/inc)

# 添加链接库查找目录，库查找序按照参数顺序从向右查
link_directories(${PROJECT_BINARY_DIR}/libs /usr.local/libs /usr/lib)

# 设置生成的库文件目录，这里我们设置成和库目录相同
set(LIBRARY_OUTPUT_PATH ${PROJECT_BINARY_DIR}/libs)

# 设置可执行文件目录，同样设成和库目录相同
set(EXECUTABLE_OUTPUT_PATH ${PROJECT_BINARY_DIR}/libs)

# 添加子目录（每个子目录下都必须有自已的CMakeLists.txt文件
#add_subdirectory(so1)
#add_subdirectory(so2)
add_subdirectory(src)
add_subdirectory(test)
