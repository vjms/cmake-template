cmake_minimum_required(VERSION 3.13)

project(proj)

set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED True)

# Set compile options
if (MSVC)
    add_compile_options(/W4 /WX)
else()
    add_compile_options(-Wall -Wextra -pedantic -Werror)
endif()

# Executable
add_executable(${PROJECT_NAME})
add_subdirectory(src)

