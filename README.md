# EX.NO:3a             CREATION FOR ECHO CLIENT AND ECHO SERVER USING TCP SOCKETS

## NAME: Suman G
## REG.NO:212223240163

## AIM:
To write a python program for creating Echo Client and Echo Server using TCP
Sockets Links.

## ALGORITHM:
1. Import the necessary modules in python</br>
2. Create a socket connection to using the socket module.</br>
3. Send message to the client and receive the message from the client using the Socket module in
 server.</br>
4. Send and receive the message using the send function in socket.</br>

## PROGRAM:
### Client
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 msg=input("Client > ")
 s.send(msg.encode())
 print("Server > ",s.recv(1024).decode())
```
### Server
```
import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
 ClientMessage=c.recv(1024).decode()
 c.send(ClientMessage.encode())
```
## OUPUT:
### Client
<img width="936" alt="Screenshot 2024-04-09 at 12 59 52 PM" src="https://github.com/aaron-h-2k5/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/144250957/cea9bc6a-91e8-487d-80b1-f37b391bd93c">

## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
