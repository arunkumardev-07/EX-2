# EX-2 IMPLEMENTATION OF STOP AND WAIT PROTOCOL

# DATE:

# AIM :
To write a python program to perform stop and wait protocol.

# ALGORITHM :
```
1. Start the program.
2. Get the frame size from the user
3. To create the frame based on the user request.
4. To send frames to server from the client side.
5. If your frames reach the server it will send ACK signal to client otherwise it will sendNACK 
   signal to client.
6. Stop the program
```

# PROGRAM :
```
Developed By: S Adithya Chowdary.
Reg. No.: 212221230100.
```

# Client:
```
import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
    i=input("Enter a data: ")
    c.send(i.encode())
    ack=c.recv(1024).decode()
    if ack:
        print(ack)
        continue
    else:
        c.close()
        break
  ```
 
# Server:
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
    print(s.recv(1024).decode())
    s.send("Acknowledgement Recived".encode())
 ```

# OUTPUT :
# Client Side:
![241416627-110f94e7-88ba-4975-8a1f-bea44b922ea2](https://github.com/arunkumardev-07/EX-2/assets/135949761/29a77a23-46b6-45fb-bca1-858bb7213255)

# Server:
![241416642-550ea1fe-fbc6-4b22-a4d6-4ad13e97d529](https://github.com/arunkumardev-07/EX-2/assets/135949761/53835624-2f2e-4e10-990a-6a857fdd37e8)

# RESULT :
Thus, python program to perform stop and wait protocol was successfully executed.



