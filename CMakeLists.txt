cmake_minimum_required(VERSION 3.0)
project(paddle-mobile)
add_definitions(-DPADDLE_MOBILE_DEBUG)
add_definitions(-DENABLE_EXCEPTION)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11")
set(CMAKE_BUILD_TYPE RelWithDebInfo)
set(CMAKE_VERBOSE_MAKEFILE ON)
set(CMAKE_EXPORT_COMPILE_COMMANDS ON)
set(CMAKE_ARCHIVE_OUTPUT_DIRECTORY build)
set(CMAKE_LIBRARY_OUTPUT_DIRECTORY build)
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY build)


# include headers

#include(ExternalProject)
#ExternalProject_Add(openblas_proj
#        GIT_REPOSITORY "https://github.com/xianyi/OpenBLAS.git"
#        GIT_TAG "v0.2.20"
#        SOURCE_DIR "openblas/"
#        BUILD_IN_SOURCE 1
#        CONFIGURE_COMMAND ""
#        BUILD_COMMAND "make" "ONLY_CBLAS=1"
#        INSTALL_COMMAND "make" "PREFIX=${CMAKE_BINARY_DIR}/" "install"
#        )
#set_target_properties(openblas_proj PROPERTIES EXCLUDE_FROM_ALL 1)

#add_dependencies(paddle-mobile openblas_proj)

# gen static

#add_dependencies(paddle-mobile openblas_proj)

ADD_EXECUTABLE(test-assembly main.cpp)
