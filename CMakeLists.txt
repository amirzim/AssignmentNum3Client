cmake_minimum_required(VERSION 3.13)
project(AssignmentNum3Client)

set(CMAKE_CXX_STANDARD 11)

add_executable(AssignmentNum3Client main.cpp
        include/connectionHandler.h
        src/connectionHandler.cpp
        src/echoClient)