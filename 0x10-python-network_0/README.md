
## PYTHON NETWORK

Python provides two levels of access to network services. At a low level, you can access the basic socket support in the underlying operating system, which allows you to implement clients and servers for both connection-oriented and connectionless protocols.

Python also has libraries that provide higher-level access to specific application-level network protocols, such as FTP, HTTP, and so on.

What are Sockets?

Consider a bidirectional communication channel, the sockets are the endpoints of this communication channel. These sockets (endpoints) can communicate within a process, between processes on the same machine, or between the processes on the different machines. Sockets use different protocols for determining the connection type for port-to-port communication between clients and servers.

Socket Programming
Socket programming is a way of connecting two nodes on a network to communicate with each other. One socket(node) listens on a particular port at an IP, while the other socket reaches out to the other to form a connection. The server forms the listener socket while the client reaches out to the server. They are the real backbones behind web browsing. In simpler terms, there is a server and a client. We can use the socket module for socket programming. For this, we have to include the socket module – 

import socket


to create a socket we have to use the socket.socket() method. 

Syntax:

socket.socket(socket_family, socket_type, protocol=0)
Where, 

socket_family: Either AF_UNIX or AF_INET
socket_type: Either SOCK_STREAM or SOCK_DGRAM.
protocol: Usually left out, defaulting to 0.



