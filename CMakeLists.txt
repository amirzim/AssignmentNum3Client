cmake_minimum_required(VERSION 3.13)
project(AssignmentNum3Client)

set(CMAKE_CXX_STANDARD 11)

add_executable(AssignmentNum3Client
        include/connectionHandler.h
        include/readFromKeyboard.h
        src/connectionHandler.cpp
        src/echoClient.cpp
        src/readFromKeyboard.cpp)