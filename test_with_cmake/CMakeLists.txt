cmake_minimum_required(VERSION 2.6)
project(test_lua_api)

# find packages
find_package(Lua 5.4 REQUIRED)

# list variables for debug
get_cmake_property(_variableNames VARIABLES)
list (SORT _variableNames)
foreach (_variableName ${_variableNames})
    message(STATUS "${_variableName}=${${_variableName}}")
endforeach()

add_executable(test_lua_api test_api.cpp)
target_link_libraries(test_lua_api ${LUA_LIBRARIES})
target_include_directories(test_lua_api PRIVATE ${LUA_INCLUDE_DIR})



