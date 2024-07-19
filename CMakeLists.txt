cmake_minimum_required(VERSION 3.6)

project(Test)

set(CMAKE_EXPORT_COMPILE_COMMANDS
    ON
)

aux_source_directory(${CMAKE_CURRENT_LIST_DIR}/src SRC)

add_executable(
    Test
    ${SRC}
)

target_include_directories(
    Test
    PRIVATE ${CMAKE_CURRENT_LIST_DIR}/inc
)
