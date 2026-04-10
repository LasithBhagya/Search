cmake_minimum_required(VERSION 4.0)
project(Search)

set(CMAKE_CXX_STANDARD 20)

set(CMAKE_CXX_FLAGS "-static")

link_libraries(ntdll shlwapi)


include_directories(
        ${CMAKE_SOURCE_DIR}/include
)

link_directories(
        # ${CMAKE_SOURCE_DIR}/lib
)

add_executable(Search
        include/SearchEngine.hpp
        
        src/main.cpp
)


target_link_libraries(${PROJECT_NAME}
        mingw32

        # PRIVATE
        # ntdll
        # shlwapi
)