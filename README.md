# 3a.CREATION FOR ECHO CLIENT AND ECHO SERVER USING TCP SOCKETS
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
CLIENT
```
import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
    clientmessage=c.recv(1024).decode()
    c.send(clientmessage.encode())
```

SERVER
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
    msg=input("Client>")
    s.send(msg.encode())
    print("server>",s.recv(1024).decode())
```
    
## OUPUT
CLIENT OUTPUT
![image](https://github.com/mdgj2005/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/145533936/ddd21865-e421-4738-9b34-6c0dafacda2e)

SERVER OUTPUT
![image](https://github.com/mdgj2005/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/145533936/8344710c-9e92-497e-9088-84f5661b190d)


## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
