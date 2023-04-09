cmake_minimum_required(VERSION 3.13)
include(pico_sdk_import.cmake)

project(hello_uart_bt C CXX ASM)

set(CMAKE_C_STANDARD 11)
set(CMAKE_CXX_STANDARD 17)
pico_sdk_init()

add_executable(hello_uart
        hello_uart.c
        )

# pull in common dependencies
target_link_libraries(hello_uart pico_stdlib)

# create map/bin/hex file etc.
pico_add_extra_outputs(hello_uart)
