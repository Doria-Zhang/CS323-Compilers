# header begin
cmake_minimum_required(VERSION 3.16.6)
project(CS323_compilers_lab01 LANGUAGES C)

set(CMAKE_C_FLAGS "${CMAKE_C_FLAGS} -fPIC")

add_library(${PROJECT_NAME}_ll
        SHARED
        linked_list.c)  

add_executable(${PROJECT_NAME}_hello.out ./hello_world.c)

add_executable(${PROJECT_NAME}_ll_main.out main.c)

target_link_libraries(${PROJECT_NAME}_ll_main.out ${PROJECT_NAME}_ll)