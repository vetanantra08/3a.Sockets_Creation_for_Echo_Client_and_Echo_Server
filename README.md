# 3a.CREATION FOR ECHO CLIENT AND ECHO SERVER USING TCP SOCKETS
##Name:R.S.Vetanantra
##Reg no: 212225040486
# AIM
To write a python program for creating Echo Client and Echo Server using TCP
Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server .
4. Send and receive the message using the send function in socket.
## PROGRAM
server
~~~
import socket
s=socket.socket()
s.bind(('localhost',8001))
s.listen(5)
c,addr=s.accept()
while True:
    ClientMessage=c.recv(1024).decode()
    c.send(ClientMessage.encode())
~~~
client
~~~
import socket

s = socket.socket()
s.connect(('localhost', 8000))

while True:
    ip = input("Enter Logical Address (IP): ")
    s.send(ip.encode())
    print("MAC Address:", s.recv(1024).decode())
~~~

## OUPUT
server
<img width="777" height="332" alt="Screenshot 2026-03-18 083936" src="https://github.com/user-attachments/assets/78dbbb61-4d98-4e18-9c2c-09711fe1c8e1" />
client
<img width="722" height="175" alt="Screenshot 2026-03-18 083957" src="https://github.com/user-attachments/assets/01249a9f-b902-443c-8db6-1b0bde3a19a4" />

## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
