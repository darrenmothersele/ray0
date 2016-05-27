cmake_minimum_required(VERSION 3.5)
project(ray1_ps)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11")

set(CMAKE_MODULE_PATH ${CMAKE_CURRENT_SOURCE_DIR}/cmake)
set(FREEIMAGE_FIND_REQUIRED, TRUE)
find_package(freeimage)
include_directories(SYSTEM ${FREEIMAGE_INCLUDE_DIRS})

include_directories(src)

set(SOURCE_FILES src/main.cc)
add_executable(ray1_ps ${SOURCE_FILES})
target_link_libraries(ray1_ps ${FREEIMAGE_LIBRARIES})
