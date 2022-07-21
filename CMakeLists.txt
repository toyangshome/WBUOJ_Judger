cmake_minimum_required (VERSION 3.0)
project (JUDGER)

file(GLOB SRC_FILES
 "${PROJECT_SOURCE_DIR}/libjudger/*.cpp" 
 "${PROJECT_SOURCE_DIR}/libjudger/*.hpp")

 add_executable(${CMAKE_PROJECT_NAME} ${SRC_FILES})
 set(CMAKE_CXX_STANDARD 11)
 