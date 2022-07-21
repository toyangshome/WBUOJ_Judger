cmake_minimum_required (VERSION 3.0)
project (
        JUDGER
        VERSION 0.1
        LANGUAGES CXX)

# Only do these if this is the main project, and not if it is included through add_subdirectory
if(CMAKE_PROJECT_NAME STREQUAL PROJECT_NAME)

  # Optionally set things like CMAKE_CXX_STANDARD, CMAKE_POSITION_INDEPENDENT_CODE here

  # Let's ensure -std=c++xx instead of -std=g++xx
  set(CMAKE_CXX_EXTENSIONS OFF)

  # Let's nicely support folders in IDEs
  set_property(GLOBAL PROPERTY USE_FOLDERS ON)

  # Testing only available if this is the main app
  # Note this needs to be done in the main CMakeLists
  # since it calls enable_testing, which must be in the
  # main CMakeLists.
  include(CTest)

endif()
file(GLOB SRC_FILES
 "${PROJECT_SOURCE_DIR}/libjudger/*.cpp" 
 "${PROJECT_SOURCE_DIR}/libjudger/*.hpp")

  # The compiled library code is here
add_subdirectory(src)

# The executable code is here
add_subdirectory(apps)

add_executable(${CMAKE_PROJECT_NAME} ${SRC_FILES})
 
