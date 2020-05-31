cmake_minimum_required(VERSION 2.8)

## Use the variable PROJECT_NAME for changing the target name
set( PROJECT_NAME "solutunnel" )

## Set our project name
project(${PROJECT_NAME})


set(CMAKE_POSITION_INDEPENDENT_CODE ON)
add_compile_options(-O2)

## Use all the *.cpp files we found under this folder for the project
FILE(GLOB SRCS "src/*.cpp")


#set(CMAKE_VERBOSE_MAKEFILE ON)
## Define the executable
add_executable(${PROJECT_NAME} ${SRCS})

target_link_libraries(${PROJECT_NAME} solunet ssl crypto)
