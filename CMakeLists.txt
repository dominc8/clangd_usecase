cmake_minimum_required(VERSION 3.23)

set(ENV{CMAKE_EXPORT_COMPILE_COMMANDS} TRUE)

project (clangd_usecase)

include_directories(${CMAKE_SOURCE_DIR}/inc)

add_library(lib1 ${CMAKE_SOURCE_DIR}/lib1/foo.cpp)
add_library(lib2 ${CMAKE_SOURCE_DIR}/lib2/foo.cpp)

add_executable(app1 ${CMAKE_SOURCE_DIR}/src/app.cpp)
add_executable(app2 ${CMAKE_SOURCE_DIR}/src/app.cpp)

target_link_libraries(app1 lib1)
target_link_libraries(app2 lib2)

