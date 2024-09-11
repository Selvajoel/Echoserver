# Echoserver
Echo server and client using python socket

# AIM:

To develop a simple webserver to serve html programming pages.

## DESIGN STEPS:

### Step 1:

Design of echo server and client using python socket

### Step 2:

Implementation using Python code

### Step 3:

Testing the server and client 

## PROGRAM:
```
Name : Vijay Shankar M
Reg no: 212222040178
```
### Server code
```
# echo-server.py
import socket
HOST = "127.0.0.1" 
PORT = 65432
with socket.socket(socket.AF_INET, socket.SOCK_STREAM) as s:
    s.bind((HOST, PORT))
    s.listen()
    conn, addr = s.accept()
    with conn:
        print(f"Connected by {addr}")
        while True:
            data = conn.recv(1024)
            if not data:
                break
            conn.sendall(data)

```
### Client Code:
```
# echo-client.py

import socket
HOST = "127.0.0.1"
PORT = 65432
with socket.socket(socket.AF_INET, socket.SOCK_STREAM) as s:
    s.connect((HOST, PORT)) 
    s.sendall(b"Vijay Shankar M,")
    s.sendall(b"212222040178")
    data = s.recv(1024)
print(f"\nRecived {data!r}")

```
## OUTPUT:
### SERVER SIDE
![server](https://github.com/user-attachments/assets/e2683c53-357b-4d3e-b81c-d1f873793428)



### CLIENT SIDE 
![client](https://github.com/user-attachments/assets/fdbe3244-5b63-4433-9819-026f59a1cadc)


## RESULT:
The program is executed successfully
