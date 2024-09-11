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
![server](https://github.com/user-attachments/assets/c313a96f-8426-46e0-a052-f89a84af375e)

### CLIENT SIDE 
![client](https://github.com/user-attachments/assets/558e1bbb-b18d-424b-a72c-a1878082e881)


## RESULT:
The program is executed successfully
