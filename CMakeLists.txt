cmake_minimum_required(VERSION 3.27)
project(lc3_vm C)

set(CMAKE_C_STANDARD 11)

add_executable(sum_program
        sum_program.c
)

add_executable(lc3_vm
        vm.c
        vm_dbg.h
)