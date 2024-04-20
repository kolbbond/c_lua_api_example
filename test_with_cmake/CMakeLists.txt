cmake_minimum_required(VERSION 3.6)
project(test_lua_api)

# add our cmake helpers directory
list(APPEND CMAKE_MODULE_PATH "$ENV{CMAKEHELPERS_DIR}")
#list(APPEND CMAKE_MODULE_PATH "${CMAKE_CURRENT_LIST_DIR}/cmake")

message(STATUS "newpath")
message(STATUS "${CMAKE_MODULE_PATH}")

# find packages
find_package(Lua 5.4 REQUIRED)
#include(PrintVariables.cmake)
include(PrintVariables)

add_executable(${PROJECT_NAME} test_api.cpp)
target_link_libraries(${PROJECT_NAME} ${LUA_LIBRARIES})
target_include_directories(${PROJECT_NAME} PRIVATE ${LUA_INCLUDE_DIR})



