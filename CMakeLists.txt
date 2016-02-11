cmake_minimum_required(VERSION 3.0)

project(universh)

# global config
set (UNIVERSH_TEST CACHE "Compile the tests?" ON)

find_package(LLVM REQUIRED)

add_subdirectory(src)

if(${UNIVERSH_TEST})
	add_subdirectory(test)
endif(${UNIVERSH_TEST})
