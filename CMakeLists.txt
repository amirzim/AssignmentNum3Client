cmake_minimum_required(VERSION 3.13)
project(AssignmentNum3Client)

set(CMAKE_CXX_STANDARD 11)
find_package(Boost COMPONENTS system filesystem thread REQUIRED)
IF (Boost_FOUND)
    include_directories(${Boost_INCLUDE_DIR})
endif()
#link_directories(${Boost_LIBRARY_DIR})
SET(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS}-std=c++11 -pthread -lboost_thread")

include_directories(include)
add_executable(AssignmentNum3Client
        include/connectionHandler.h
        include/readFromKeyboard.h
        src/connectionHandler.cpp
        src/echoClient.cpp
        src/readFromKeyboard.cpp src/readFromServer.cpp src/readFromKeyboard.cpp include/readFromServer.h)

target_link_libraries( AssignmentNum3Client LINK_PUBLIC ${Boost_LIBRARIES} )