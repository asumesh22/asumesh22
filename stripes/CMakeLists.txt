cmake_minimum_required(VERSION 3.0.0)
project(stripes VERSION 0.1.0)

include(CTest)
enable_testing()

find_package( OpenCV REQUIRED )
include_directories( ${OpenCV_INCLUDE_DIRS} )

add_executable(stripes main.cpp)

target_link_libraries(stripes ${OpenCV_LIBS})

set(CPACK_PROJECT_NAME ${PROJECT_NAME})
SET(CPACK_PROJECT_VERSION ${PROJECT_VERSION})
include(CPack)