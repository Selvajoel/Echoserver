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
Name :selvajoel s
Reg no: 212222220040
```
### Server code
```
# echo-server.py
import socket

HOST = "127.0.0.1"  # Standard loopback interface address (localhost)
PORT = 65432  # Port to listen on (non-privileged ports are > 1023)

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
    s.sendall(b"Selve Joel,")
    s.sendall(b"212222220040")
    data = s.recv(1024)
print(f"\nRecived {data!r}")
```
## OUTPUT:
### SERVER SIDE
![WhatsApp Image 2024-09-11 at 09 31 36_d27bff7a](https://github.com/user-attachments/assets/9abebb5e-2360-4daa-8540-2bba95dea94a)

### CLIENT SIDE 
![WhatsApp Image 2024-09-11 at 09 31 37_beb2c743](https://github.com/user-attachments/assets/d19db4a3-7bf6-4959-90d7-aaf0eada004c)


## RESULT:
The program is executed successfully
