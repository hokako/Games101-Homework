cmake_minimum_required(VERSION 3.10)
project(Rasterizer1)

set(CMAKE_CXX_STANDARD 17)

# Use the system OpenCV package (works on Linux). If you have a local OpenCV,
# set OpenCV_DIR or install OpenCV development packages so find_package finds it.
find_package(OpenCV REQUIRED)

include_directories(${OpenCV_INCLUDE_DIRS} ./../)

add_executable(Rasterizer1 main.cpp rasterizer.hpp rasterizer.cpp Triangle.hpp Triangle.cpp)
target_link_libraries(Rasterizer1 ${OpenCV_LIBS})



