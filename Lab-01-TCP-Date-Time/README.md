# Lab 1: TCP Client-Server Program to Display Current Date and Time

## Objective

* To understand the fundamentals of TCP socket programming.
* To establish communication between a TCP client and server.
* To send the current date and time from the server to the client.
* To learn the use of POSIX socket system calls.

---

## Theory

TCP (Transmission Control Protocol) is a connection-oriented protocol that provides reliable, ordered, and error-free communication between two devices over a network.

In this experiment, the server creates a socket, binds it to a specific port, and waits for incoming client connections. When a client connects, the server retrieves the current system date and time using the C Standard Library and sends it to the client. The client receives the data and displays it on the terminal.

---

## System Calls Used

| Function    | Description                                          |
| ----------- | ---------------------------------------------------- |
| `socket()`  | Creates a new socket.                                |
| `bind()`    | Assigns an IP address and port number to the socket. |
| `listen()`  | Waits for incoming client connection requests.       |
| `accept()`  | Accepts a connection from a client.                  |
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

Start the server:

```bash
./server 5000
```

Open another terminal and start the client:

```bash
./client 127.0.0.1 5000
```

---

## Expected Output

### Server

```text
Server waiting for client connection...
Client connected successfully.
Current date and time sent to client.
```

### Client

```text
Connected to server.

Current Date and Time:

Sun Jun 20 10:35:48 2026
```

---

## Learning Outcomes

* Understood the Client-Server communication model.
* Learned the working of TCP sockets.
* Implemented reliable communication using TCP.
* Practiced the use of Linux socket programming APIs.
* Successfully transferred data from server to client.

---

## Conclusion

The experiment successfully demonstrated TCP client-server communication using the POSIX Socket API. The server accepted a client connection, retrieved the current system date and time, and transmitted it reliably to the client. This lab provided practical experience with socket creation, connection establishment, data transmission, and connection termination in C under Linux.
