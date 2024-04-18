# 3b.CREATION FOR CHAT USING TCP SOCKETS
Name:R.Sabarinath 
Register No:212223100048
## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM
## CLIENT
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 msg=input("Client > ")
 s.send(msg.encode())
 print("Server > ",s.recv(1024).decode())
```
## SERVER
```
import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
 ClientMessage=c.recv(1024).decode()
 print("Client > ",ClientMessage)
 msg=input("Server > ")
 c.send(msg.encode())
```
## OUPUT
## CLIENT
![image](https://github.com/Sabari-2005/3b_CHAT_USING_TCP_SOCKETS/assets/139338709/4a0d481c-1a24-4826-b9a2-43cedd9707c8)
## SERVER
![image](https://github.com/Sabari-2005/3b_CHAT_USING_TCP_SOCKETS/assets/139338709/53f78f7a-b70d-43d8-a9d9-4877cc41735d)

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully created and executed.
