cmake_minimum_required(VERSION 3.6)
project(proxyServer)

set(CMAKE_CXX_STANDARD 14)

set(SOURCE_FILES ProxyServer.cpp
        SessionWrapper.h
        ProxyStats.h
        ProxyHandler.cpp
        ProxyHandler.h)

include_directories(/user/local/include)
link_directories(/usr/local/lib)

add_executable(proxyServer ${SOURCE_FILES})

target_link_libraries(proxyServer folly proxygenhttpserver glog gflags pthread double-conversion wangle uuid pthread libproxygencurl.a)