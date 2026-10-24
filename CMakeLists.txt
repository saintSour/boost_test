cmake_minimum_required(VERSION 3.15)

#set(VCPKG_MANIFEST_INSTALL ON CACHE BOOL "Включение автоматической установки vcpkg" FORCE)

project(main LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

find_package(Boost REQUIRED COMPONENTS program_options)

add_executable(main
    src/main.cpp
)

target_link_libraries(main PRIVATE
    Boost::program_options
)
