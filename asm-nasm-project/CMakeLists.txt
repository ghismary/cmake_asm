cmake_minimum_required(VERSION 3.22)

project(ASM-NASM-Project VERSION 0.1)

enable_language(ASM_NASM)

add_library(asm-nasm OBJECT "hello.asm")
