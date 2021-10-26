project(soTest)
set(st test.cpp)
#include_directories(../src/so1/inc)
# 生成可执行文件
add_executable(st test.cpp)
target_link_libraries(st so2 so1)
