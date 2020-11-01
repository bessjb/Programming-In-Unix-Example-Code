cmake_minimum_required(VERSION 3.0.0)
project(ls VERSION 0.1.0)

include(CTest)
enable_testing()

include_directories("${CMAKE_CURRENT_SOURCE_DIR}/include") 

set(SOURCES src/chapter_1/ls.c include/apue.h include/apue.c)

add_executable(ls ${SOURCES})

set(CPACK_PROJECT_NAME ${PROJECT_NAME})
set(CPACK_PROJECT_VERSION ${PROJECT_VERSION})
include(CPack)
