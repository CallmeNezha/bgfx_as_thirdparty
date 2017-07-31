cmake_minimum_required(VERSION 3.7)
project(bgfx_test)

set(SOURCE_FILES helloworld.cpp)

add_subdirectory("thirdparty/bgfx.cmake")
add_executable(bgfx_test ${SOURCE_FILES})
include_directories("thirdparty/bgfx.cmake/bgfx/examples")
target_link_libraries(bgfx_test bgfx example-common)