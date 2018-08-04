cmake_minimum_required(VERSION 3.0)

project(TestSol2)

find_package(lua REQUIRED)
message(Lua include: ${LUA_INCLUDE_PREFIX}/include)
include_directories(${LUA_INCLUDE_PREFIX}/include)

add_executable(TestSol2 TestSol2.cpp sol.hpp lua.hpp)

target_link_libraries(TestSol2 ${LUA_LIBRARY})
