cmake_minimum_required(VERSION 3.5)
project(Environment)
set( CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11" )
set( CMAKE_RUNTIME_OUTPUT_DIRECTORY "${CMAKE_BINARY_DIR}/bin" )
set( CMAKE_LIBRARY_OUTPUT_DIRECTORY "${CMAKE_BINARY_DIR}/lib" )
set( CMAKE_ARCHIVE_OUTPUT_DIRECTORY "${CMAKE_BINARY_DIR}/lib" )


file( GLOB PROJECT_SOURCE_FILES *.cpp *.h )

set( PROJECT_EXTRA_LIBS    "" )


add_subdirectory("thirdparty/bgfx.cmake")
add_executable(${PROJECT_NAME} ${PROJECT_SOURCE_FILES})
target_link_libraries(${PROJECT_NAME} bgfx example-common)
