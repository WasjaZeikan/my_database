cmake_minimum_required(VERSION 3.28.0)
project(MyDatabase VERSION 0.1.0 LANGUAGES C)

include(CTest)
enable_testing()

set(SOURCES_FILES main.c
buffer.c
prepocessor.c
utility.c)
add_executable(MyDatabase ${SOURCES_FILES})

set(CPACK_PROJECT_NAME ${PROJECT_NAME})
set(CPACK_PROJECT_VERSION ${PROJECT_VERSION})
include(CPack)

target_include_directories(MyDatabase PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/include)