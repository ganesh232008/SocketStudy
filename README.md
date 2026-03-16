# Ex.No:1a  			Study of Socket Programming

## Date:29/01/2026

## Roll No: 212225230072

## Aim: 
To perform a study on Socket Programming
## Introduction:

 	Socket programming is a crucial aspect of network communication, allowing for data exchange between computers over a network. It forms the backbone of various networked applications, enabling communication between clients and servers. This study explores the fundamental concepts of socket programming, its use cases, and provides a practical example to demonstrate its implementation.
## Understanding Socket Programming:
	Socket programming involves the use of sockets, which serve as endpoints for communication. A socket is identified by an IP address and a port number, and it facilitates data transfer between a client and a server. The two main types of sockets are Stream Sockets, which provide a reliable, connection-oriented communication, and Datagram Sockets, which are connectionless and suitable for scenarios where reliability is less critical.
## Key Concepts in Socket Programming:
1.Sockets
•	A socket is a software representation of a communication endpoint in a network.
•	It is identified by an IP address and a port number.
•	Sockets can be classified into two main types: Stream Sockets and Datagram Sockets.
•	Stream Sockets provide a reliable, connection-oriented communication, while Datagram Sockets are connectionless and operate in a best-effort mode.

2. Client-Server Model

•	Socket programming typically follows the client-server model.
•	The server listens for incoming connections from clients, while clients initiate connections to the server.
•	Servers are passive, waiting for connection requests, and clients are active, initiating communication.

3, TCP/IP Protocol:

•	Transmission Control Protocol (TCP) and Internet Protocol (IP) are the foundational protocols for socket programming.
•	TCP provides reliable, connection-oriented communication, ensuring data integrity and order.
•	IP facilitates the routing of data between devices in a network.

4.Basic Socket Functions:

•	Socket programming involves a set of functions provided by the operating system or programming language to create, bind, listen, accept, connect, send, and receive data through sockets.
•	Examples of functions include socket(), bind(), listen(), accept(), connect(), send(), and recv().

## Server-Side Operations:

•	Servers create a socket using socket() and bind it to a specific IP address and port using bind().
•	They then listen for incoming connections with listen() and accept connections with accept().
•	Once a connection is establi
•	shed, servers can send and receive data using send() and recv().

## Client –Server Operations

Clients create a socket using socket() and connect to a server using connect().
After establishing a connection, clients can send and receive data using send() and recv().

## Use Cases of Socket Programming:
Socket programming finds applications in various domains, including web development, file transfer protocols, online gaming, and real-time communication. It is the foundation for protocols like HTTP, FTP, and SMTP, which power the internet. Socket programming enables the development of both server and client applications, facilitating the exchange of information between devices in a networked environment.

## Algorithm
1.Start the program.

2.Import the required Python library socket.

3.Create a TCP socket using socket.socket().

4.Define the IP address (127.0.0.1) and port number (8000).

5.Bind the socket with the IP address and port number.

6.Put the server in listening mode using listen().

7.Wait for the client connection request.

8.Accept the connection using accept().

9.Receive data from the client using recv().

10.Process the received message.

11.Send a response back to the client using send().

12.Continue communication until the client stops sending data.

13.Close the client connection.

14.Close the server socket.

15.Stop the program.

## Input:
Server:
```
import socket             
# next create a socket object 
s = socket.socket()         
print ("Socket successfully created")
port = 12345                
s.bind(('', port))         
print ("socket binded to %s" %(port)) 
s.listen(5)     
print ("socket is listening")            
while True: 
  c, addr = s.accept()     
  print ('Got connection from', addr )
  c.send('Thank you for connecting'.encode()) 
  # Close the connection with the client 
c.close()
```
Client:
```
# Import socket module 
import socket             

# Create a socket object 
s = socket.socket()         

# Define the port on which you want to connect 
port = 12345                

# connect to the server on local computer 
s.connect(('127.0.0.1', port)) 

# receive data from the server and decoding to get the string.
print (s.recv(1024).decode())
# close the connection 
s.close()
```
## Output:
 Client:
<img width="953" height="937" alt="Screenshot 2026-01-30 185231" src="https://github.com/user-attachments/assets/52cb1c36-296f-4561-881a-a647e9b9cdaf" />

Server:

<img width="1097" height="921" alt="Screenshot 2026-01-30 185252" src="https://github.com/user-attachments/assets/ffc4228f-6715-4771-b3d3-b3c0cb8d6b28" />

## Result:
Thus the study of Socket Programming Completed Successfully
