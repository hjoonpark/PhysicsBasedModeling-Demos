cmake_minimum_required (VERSION 3.0)
set (CMAKE_CXX_STANDARD 11)

project (Finite-Element-Tests)

set (CMAKE_CXX_FLAGS "-Wno-deprecated ${CMAKE_CXX_FLAGS}")

add_definitions(-DBUILD_COMPONENT_SRC_PREFIX="" -DBUILD_OPTLEVEL_DEV)

set(USD_ROOT_DIR /nobackup/joon/local/USD)
set(USD_LIB_DIR ${USD_ROOT_DIR}/lib/)
set(USD_INC_DIR ${USD_ROOT_DIR}/include/)

add_subdirectory(tests)
