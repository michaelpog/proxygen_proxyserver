# proxygen_proxyserver

This repo is a clone of the Proxygen proxyServer
I created it to share with Facebook proxygen to show the Debug and Release compile version discrepancies.

DEBUG:
Building:
/home/michaelpog/clion-2016.3.2/bin/cmake/bin/cmake --build /home/michaelpog/development/proxyServer/cmake-build-debug --target proxyServer -- -j 2
[ 33%] Building CXX object CMakeFiles/proxyServer.dir/ProxyHandler.cpp.o
[ 66%] Building CXX object CMakeFiles/proxyServer.dir/ProxyServer.cpp.o
[100%] Linking CXX executable proxyServer
[100%] Built target proxyServer

Running:
/home/michaelpog/development/proxyServer/cmake-build-debug/proxyServer --logtostderr --redirect_url=http://127.0.0.1:9000

Output:
I0309 10:35:58.475397 32967 ProxyHandler.cpp:63] Trying to connect to 127.0.0.1:9000
I0309 10:35:58.478464 32967 ProxyHandler.cpp:92] Established [local = 127.0.0.1:48500, 127.0.0.1:9000 = upstream]
I0309 10:35:58.478554 32967 ProxyHandler.cpp:95] Forwarding client request: /http://127.0.0.0.1:8080 to server
I0309 10:35:58.478884 32967 ProxyHandler.cpp:84] Forwarding client EOM to server
I0309 10:35:58.478993 32967 ProxyHandler.cpp:115] Forwarding 301 response to client
I0309 10:35:58.479065 32967 ProxyHandler.cpp:121] Forwarding 58 body bytes to client
I0309 10:35:58.479089 32967 ProxyHandler.cpp:128] Forwarding server EOM to client
I0309 10:35:58.479110 32967 SessionWrapper.h:55] max: 1 current:0


Release:
Building:
/home/michaelpog/clion-2016.3.2/bin/cmake/bin/cmake --build /home/michaelpog/development/proxyServer/cmake-build-release --target proxyServer -- -j 2
[ 33%] Building CXX object CMakeFiles/proxyServer.dir/ProxyHandler.cpp.o
[ 66%] Building CXX object CMakeFiles/proxyServer.dir/ProxyServer.cpp.o
[100%] Linking CXX executable proxyServer
[100%] Built target proxyServer

Running:
/home/michaelpog/development/proxyServer/cmake-build-release/proxyServer --logtostderr --redirect_url=http://127.0.0.1:9000
OUTPUT:

I0309 10:21:00.508827 32531 ProxyHandler.cpp:63] Trying to connect to 127.0.0.1:9000
I0309 10:21:00.509608 32531 ProxyHandler.cpp:92] Established [local = 127.0.0.1:48476, 127.0.0.1:9000 = upstream]
I0309 10:21:00.509634 32531 ProxyHandler.cpp:95] Forwarding client request: /http://127.0.0.0.1:8080 to server
I0309 10:21:00.511958 32531 ProxyHandler.cpp:84] Forwarding client EOM to server
I0309 10:21:00.512020 32531 ProxyHandler.cpp:115] Forwarding 301 response to client
I0309 10:21:00.512053 32531 ProxyHandler.cpp:121] Forwarding 58 body bytes to client
I0309 10:21:00.512068 32531 ProxyHandler.cpp:128] Forwarding server EOM to client
I0309 10:21:00.512084 32531 SessionWrapper.h:55] max: 0 current:1
