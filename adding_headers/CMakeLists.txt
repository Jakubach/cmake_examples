cmake_minimum_required(VERSION 3.5)

project(adding_headers LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

# Useful CMake options for Qt projects
set(CMAKE_INCLUDE_CURRENT_DIR ON)
set(CMAKE_AUTOMOC ON)

# Create a list with all .cpp source files
set(SOURCES
   src/athlete.cpp
   src/main.cpp)

set(HEADERS
    include/athlete.h)

# Create executable with all necessary source files
add_executable(${PROJECT_NAME} ${SOURCES} ${HEADERS})
target_include_directories(${PROJECT_NAME} PUBLIC include)

