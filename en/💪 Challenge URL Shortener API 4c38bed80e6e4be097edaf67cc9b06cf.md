# 💪 Challenge: URL Shortener API

## ⭐ Goal

In this challenge, you will implement a multi-client chat server using TCP sockets. The server should be able to handle multiple client connections simultaneously, allowing users to join chat rooms, send messages to all participants in their room, and leave the chat when they're done.

This project will test your understanding of network programming, concurrency, and socket communication in your chosen programming language.

## 🚨 Requirements

1. Implement a chat server that can handle multiple client connections concurrently.
2. The server should support the following commands from clients:
    - `/join <room_name>`: Join a specific chat room
    - `/leave`: Leave the current chat room
    - `/quit`: Disconnect from the server
    - Any other message should be broadcast to all users in the same room
3. The server should maintain a list of active chat rooms and the clients in each room.
4. When a client joins a room, send a welcome message to that client and notify other clients in the room.
5. When a client leaves a room or disconnects, notify other clients in the room.
6. Implement proper error handling for invalid commands and network issues.
7. Ensure thread-safe operations when managing shared resources (e.g., room lists, client lists).

## 💼 Usage

### Input

The server should accept incoming connections on a specified port (e.g., 8888).

Clients should be able to connect to the server using a TCP client (e.g., telnet or a custom client implementation) and send the following commands:

```
/join <room_name>
/leave
/quit
<message>
```

### Output

The server should send appropriate responses to clients based on their actions:

- When a client joins a room:
    
    ```
    Welcome to room <room_name>!
    Current users: <user1>, <user2>, ...
    
    ```
    
- When a client sends a message:
    
    ```
    <username>: <message>
    ```
    
- When a client leaves a room:
    
    ```
    <username> has left the room.
    ```
    
- When a client disconnects:
    
    ```
    <username> has disconnected.
    ```
    

## 🧪 Testing

To test your implementation, follow these steps:

1. Start the chat server on a specified port.
2. Connect multiple clients to the server using a TCP client.
3. Test the following scenarios:
a. Clients joining different rooms
b. Clients sending messages within their rooms
c. Clients leaving rooms
d. Clients disconnecting from the server
e. Multiple clients performing actions concurrently
4. Verify that messages are correctly broadcasted within rooms and that join/leave notifications are sent appropriately.
5. Test error handling by sending invalid commands and simulating network issues.

## 🍥 Bonus

For extra credit, implement the following features:

1. Private messaging: Allow clients to send private messages to specific users.
2. User authentication: Implement a simple username/password system for clients to log in before joining chat rooms.
3. Persistent chat history: Store chat messages for each room and provide a way for clients to request recent message history when joining a room.
4. Server commands: Implement administrative commands that can be run on the server to manage rooms and users.
5. Chat room moderation: Allow for the designation of room moderators who can kick or ban users from a room.
6. File transfer: Enable clients to send small files to other users in the same room.
7. Encryption: Implement end-to-end encryption for messages sent between clients.