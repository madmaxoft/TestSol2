cmake_minimum_required(VERSION 3.0)

project(TestSol2)

find_package(lua REQUIRED)
message(Lua include: ${LUA_INCLUDE_PREFIX}/include)
include_directories(${LUA_INCLUDE_PREFIX}/include)

# We're using Lua in C++ mode:
add_definitions(-DSOL_USING_CXX_LUA)

add_executable(TestSol2 TestSol2.cpp sol.hpp)

target_link_libraries(TestSol2 lua)
