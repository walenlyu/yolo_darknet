cmake_minimum_required(VERSION 2.6) # set the minimal version of the cmake 

project(yolo_darknet)# set the name of the project 

#add_definitions(-std=c++11)

#option(CUDA_USE_STATIC_CUDA_RUNTIME OFF)
#set(CMAKE_CXX_STANDARD 11)
#set(CMAKE_BUILD_TYPE Debug)


#set(OpenCV_DIR "/home/walen/opencv/opencv_cuda")
set(OpenCV_DIR "C:\\software\\opencv451\\opencv451_2019_64\\install")
Find_package(OpenCV REQUIRED)


include_directories(${OpenCV_INCLUDE_DIRS})

#set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11 -Wall -Ofast -Wfatal-errors -D_MWAITXINTRIN_H_INCLUDED")


add_executable(yolo_darknet ${PROJECT_SOURCE_DIR}/yolo_darknet.cpp )  #生成可执行文件
target_link_libraries(yolo_darknet ${OpenCV_LIBS}) #将生成可执行文件与对应库文件链接起来

#add_definitions(-O2 -pthread)

