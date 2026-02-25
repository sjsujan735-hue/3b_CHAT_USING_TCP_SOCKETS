# 3b.CREATION FOR CHAT USING TCP SOCKETS
## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM
## SERVER:
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
## CLIENT:
```

import socket 
s=socket.socket() 
s.connect(('localhost',8000)) 
while True: 
    msg=input("Client > ") 
    s.send(msg.encode()) 
    print("Server > ",s.recv(1024).decode())
```

## OUTPUT:
## SERVER:
<img width="1171" height="273" alt="image" src="https://github.com/user-attachments/assets/1a00e8cb-6d80-46ef-a0e8-c03ee538c500" />
## CLIENT:
<img width="1156" height="270" alt="Screenshot 2026-02-25 111814" src="https://github.com/user-attachments/assets/2690127f-8a10-4ae4-878d-9e2bbd3eb255" />



## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
