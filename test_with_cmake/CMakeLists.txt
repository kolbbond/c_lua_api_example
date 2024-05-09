cmake_minimum_required(VERSION 3.6)
project(test_lua_api)

# find packages
find_package(Lua 5.4 REQUIRED)

add_executable(${PROJECT_NAME} test_api.cpp)
target_link_libraries(${PROJECT_NAME} ${LUA_LIBRARIES})
target_include_directories(${PROJECT_NAME} PRIVATE ${LUA_INCLUDE_DIR})



