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
```
import socket
s=socket.socket()
s.bind(('localhost',800))
s.listen(5)
c,addr=s.accept()
address={"165.165.80.80":"6A:08:AA:C2","165.165.79.1":"8A:BC:E3:FA"};
while True:
    ip=c.recv(1024).decode()
    try:
        c.send(address[ip].encode())
    except KeyError:
        c.send("Not Found".encode())
```
# SERVER:
```
import socket
s=socket.socket()
s.connect(('localhost',800))
print(s.getsockname())
print(s.recv(1024).decode())
s.send("acknowledge recived from the server".encode())
```
# OUTPUT:
# CLIENT SIDE:
![Client 2](https://github.com/balar2004/19CS406-EX-1/assets/118791778/2706cc22-6a70-46db-b907-11f7362367a7)
# SERVER SIDE:
![Server 2](https://github.com/balar2004/19CS406-EX-1/assets/118791778/8ecd4b16-bf99-44e7-b9f1-d0996ec93f9f)
# RESULT:
Thus, python program to perform stop and wait protocol was successfully executed.
