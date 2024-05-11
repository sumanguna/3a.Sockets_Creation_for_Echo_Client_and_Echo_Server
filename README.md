# EX.NO:3a             CREATION FOR ECHO CLIENT AND ECHO SERVER USING TCP SOCKETS

## AIM:
To write a python program for creating Echo Client and Echo Server using TCP
Sockets Links.

## NAME: KARTHIKEYAN R
## REG.NO:212222240046

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
![image](https://github.com/Yuvaranithulasingam/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/121418522/e28cbeca-aca7-45bd-9a14-9d0166954a0d)

## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
