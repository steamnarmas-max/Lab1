cmake_minimum_required(VERSION 3.15)

if(NOT DEFINED PROJECT_VERSION)
    set(PROJECT_VERSION "1.0.0")
endif()

project(Lab1 VERSION ${PROJECT_VERSION} LANGUAGES CXX)

configure_file(
    "${CMAKE_CURRENT_SOURCE_DIR}/main.cpp.in"
    "${CMAKE_CURRENT_BINARY_DIR}/main.cpp"
    @ONLY
)


add_executable(Lab1 "${CMAKE_CURRENT_BINARY_DIR}/main.cpp")

