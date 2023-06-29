cmake_minimum_required(VERSION 3.22)

project(ASM-Project VERSION 0.1)

enable_language(ASM)

add_library(asm OBJECT hello.S)
