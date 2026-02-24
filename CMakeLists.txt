cmake_minimum_required(VERSION 3.5)
project(ImageBasedModellingEdu)
set(CMAKE_MODULE_PATH "${CMAKE_CURRENT_SOURCE_DIR}/cmake/" ${CMAKE_MODULE_PATH})

# Eigen (required)
# 手动指定Eigen的路径
set(EIGEN_INCLUDE_DIRS "C:/Users/m30040020/tools/cppPrebuildLibs/eigen-3.4.0")
# find_package(Eigen REQUIRED)
include_directories(${EIGEN_INCLUDE_DIRS})
add_definitions(-DEIGEN_USE_NEW_STDVECTOR -DEIGEN_YES_I_KNOW_SPARSE_MODULE_IS_NOT_STABLE_YET)


set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_FLAGS "-fPIC")

add_subdirectory(core)
add_subdirectory(util)
add_subdirectory(features)
add_subdirectory(sfm)
add_subdirectory(mvs)
add_subdirectory(examples)
add_subdirectory(surface)
add_subdirectory(texturing)
add_subdirectory(3rdParty/mrf)
add_subdirectory(3rdParty/coldet)
add_subdirectory(3rdParty/gco)
#add_subdirectory(3rdParty/rayint)
#add_subdirectory(3rdParty/eigen)
#add_subdirectory(3rdParty/mapmap)