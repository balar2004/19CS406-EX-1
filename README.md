# 19CS406-EX-1 STUDY OF SOCKET PROGRAMMING WITH CLIENT-SERVER MODEL
# AIM:
To write a python program to perform stop and wait protocol
# ALGORITHM:
# Server:
1. Create a server socket and bind it to port.
2. Listen for new connection and when a connection arrives, accept it.
3. Send server‟s date and time to the client.
4. Read client‟s IP address sent by the client.
5. Display the client details.
6. Repeat steps 2-5 until the server is terminated.
7. Close all streams.
8. Close the server socket.
9. Stop.
# Client:
1. Create a client socket and connect it to the server‟s port number.
2. Retrieve its own IP address using built-in function.
3. Send its address to the server.
4. Display the date & time sent by the server.
5. Close the input and output streams.
6. Close the client socket.
7. Stop.
# PROGRAM:
# CLIENT:

# SERVER:

# OUTPUT:
# CLIENT SIDE:

# SERVER SIDE:

# RESULT:
Thus, python program to perform stop and wait protocol was successfully executed.
