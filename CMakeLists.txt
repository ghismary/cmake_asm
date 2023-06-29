cmake_minimum_required(VERSION 3.22)

project(CMakeASM VERSION 0.1 LANGUAGES C)

option(ENABLE_ASM_NASM_PROJECT OFF)
option(ENABLE_ASM_PROJECT OFF)

set(SOURCES dummy.c)

if(ENABLE_ASM_NASM_PROJECT)
  add_subdirectory("asm-nasm-project")
  list(APPEND SOURCES $<TARGET_OBJECTS:asm-nasm>)
endif()
if(ENABLE_ASM_PROJECT)
  add_subdirectory("asm-project")
  list(APPEND SOURCES $<TARGET_OBJECTS:asm>)
endif()

add_library(cmake-asm ${SOURCES})
