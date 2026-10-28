# Client-Server Model — Study Notes

## 1. Definition

The Client-Server Model is a network architecture in which a client requests a service or resource and a server provides a response.

## 2. Components

- Client: Sends requests.
- Server: Receives requests and sends responses.
- Socket: Communication endpoint.
- IP address: Identifies the destination host or interface.
- Port: Identifies the service endpoint.
- Protocol: Defines communication rules.

## 3. TCP vs UDP

**TCP**
- Connection-oriented.
- Reliable and ordered delivery.
- Used in this project.

**UDP**
- Connectionless.
- Does not guarantee delivery or ordering.
- Commonly used in DNS queries, streaming, and real-time applications.

## 4. Python Socket Functions

- `socket()` — Creates a socket.
- `bind()` — Assigns an address to the server socket.
- `listen()` — Waits for incoming connections.
- `accept()` — Accepts a connection.
- `connect()` — Connects the client to the server.
- `sendall()` — Sends bytes.
- `recv()` — Receives bytes.
- `close()` — Closes the socket.

## 5. Important Terms

- `127.0.0.1`: IPv4 loopback address.
- `5000`: Port used by this example.
- `1024`: Maximum number of bytes requested in one `recv()` call.
- `encode()`: Converts a string into bytes.
- `decode()`: Converts received bytes into a string.

## 6. Request-Response Flow

1. Start the server.
2. Create and bind the server socket.
3. Listen for client connections.
4. Start the client.
5. Establish a TCP connection.
6. Send a message.
7. Receive and display the response.
8. Close the connection.

## 7. Viva Questions

**Q1. What is a client?**  
A client requests services or data from a server.

**Q2. What is a server?**  
A server receives client requests and provides responses.

**Q3. What is a socket?**  
A socket is a communication endpoint used to send and receive data.

**Q4. Why is TCP used?**  
TCP provides reliable, ordered byte-stream communication.

**Q5. What does localhost mean?**  
It refers to the same computer, typically through a loopback address.

**Q6. What is a port number?**  
A port number identifies a transport-layer endpoint on a host.

**Q7. What does `bind()` do?**  
It associates a socket with a local IP address and port.

**Q8. What does `accept()` do?**  
It accepts an incoming connection and returns a connected socket.

**Q9. Can this project communicate between two computers?**  
Yes. Configure the server to listen on an appropriate network interface and connect using its reachable IP address, subject to firewall and network settings.

**Q10. What is the main limitation of this version?**  
It handles one client connection and then exits.
