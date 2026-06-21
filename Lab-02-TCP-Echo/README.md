# Lab 2: TCP Echo Client-Server Program Using Socket Programming

## Objective

* To understand the implementation of a TCP Echo Client-Server application.
* To establish communication between a TCP client and server.
* To send messages from the client to the server.
* To receive the same message (echo) back from the server.
* To learn the use of POSIX socket system calls in C.

---

## Theory

A TCP Echo Server is one of the simplest client-server applications used to demonstrate socket programming. The server waits for a client connection and receives a message sent by the client. It then sends the same message back to the client without modification. This process is known as **echoing**.

The client establishes a TCP connection with the server, sends a message, waits for the server's response, and displays the echoed message on the terminal.

---

## System Calls Used

| Function    | Description                                          |
| ----------- | ---------------------------------------------------- |
| `socket()`  | Creates a TCP socket.                                |
| `bind()`    | Assigns an IP address and port number to the socket. |
| `listen()`  | Waits for incoming client connections.               |
| `accept()`  | Accepts a client connection request.                 |
| `connect()` | Establishes a connection with the server.            |
| `read()`    | Receives data from the socket.                       |
| `write()`   | Sends data through the socket.                       |
| `close()`   | Closes the socket connection.                        |

---

## Compilation

Compile the server and client programs using GCC.

```bash
gcc server.c -o server
gcc client.c -o client
```

---

## Execution

### Start the Server

```bash
./server 5000
```

### Start the Client

Open another terminal and run:

```bash
./client 127.0.0.1 5000
```

---

## Sample Output

### Server

```text
Server waiting for client connection...
Client connected successfully.
Received: Hello Server
Echo sent to client.
```

### Client

```text
Connected to server.

Enter message:
Hello Server

Echo from Server:
Hello Server
```

---

## Output Screenshot

![Lab 2 Output](Output/output.png)

---

## Learning Outcomes

* Understood the working of a TCP Echo Client-Server application.
* Learned to establish reliable communication using TCP sockets.
* Implemented message transmission and reception using socket programming.
* Gained practical experience with POSIX socket APIs in Linux.
* Improved understanding of client-server communication in C.

---

## Conclusion

This experiment successfully demonstrated the implementation of a TCP Echo Client-Server application using socket programming in C. The client established a connection with the server, transmitted a message, and received the same message back from the server. The lab reinforced the concepts of reliable communication, socket creation, connection management, and data exchange using the TCP protocol.
