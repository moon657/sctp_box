cmake_minimum_required ( VERSION 2.8 )

project (sctp_sandbox)

set(CMAKE_CPP_FLAGS  "${CMAKE_CPP_FLAGS} -std=c++17")
find_package(Threads REQUIRED)

add_executable(server server.cc common.h)
add_executable(client client.cc common.h)
target_link_libraries(server ${CMAKE_THREAD_LIBS_INIT})
