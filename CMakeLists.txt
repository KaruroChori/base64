cmake_minimum_required(VERSION 3.10)
project(base64 VERSION 1.0.0 DESCRIPTION "Header-base base64 helper functions")
set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

#add_library(base64 SHARED ...)
add_library(base64 INTERFACE)
target_include_directories(base64 INTERFACE include)

include(GNUInstallDirs)

install(TARGETS base64
    LIBRARY DESTINATION ${CMAKE_INSTALL_LIBDIR}
    PUBLIC_HEADER DESTINATION ${CMAKE_INSTALL_INCLUDEDIR})
