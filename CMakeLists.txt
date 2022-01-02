cmake_minimum_required(VERSION 2.8.12)
project(sql)

add_definitions("-std=c++14")
set(CMAKE_CXX_STANDARD:14)

include(${CMAKE_BINARY_DIR}/conanbuildinfo.cmake)
conan_basic_setup()

add_executable(sql sql.cpp)
target_link_libraries(sql ${CONAN_LIBS} mysqlclient)
