# ./so2/CMakeLists.txt

project(soTest)
set(so2 so2.cpp)
# 添加include目录，本例头文件在./目录下，所以直接取${PROJECT_SOURCE_DIR}/
include_directories(../so1/inc)
add_library(so2 SHARED ${so2})

# link so1
target_link_libraries(so2 so1)
