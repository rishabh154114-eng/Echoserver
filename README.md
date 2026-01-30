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

# echo-server.py </br>

import socket </br>
HOST = "127.0.0.1"  # Standard loopback interface address (localhost) </br>
PORT = 65432  # Port to listen on (non-privileged ports are > 1023) </br>
with socket.socket(socket.AF_INET, socket.SOCK_STREAM) as s: </br>
    s.bind((HOST, PORT)) </br>
    s.listen() </br>
    conn, addr = s.accept() </br>
    with conn: </br>
        print(f"Connected by {addr}") </br>
        while True: </br>
            data = conn.recv(1024) </br>
            if not data: </br>
                break </br>
            conn.sendall(data) </br>


# echo-client.py</br>


import socket</br>
HOST = "127.0.0.1"  # The server's hostname or IP address</br>
PORT = 65432  # The port used by the server</br>

with socket.socket(socket.AF_INET, socket.SOCK_STREAM) as s:</br>
    s.connect((HOST, PORT))</br>
    s.sendall(b"Rishabh Srivatsav 212224113001")</br>
    data = s.recv(1024)</br>
print(f"Received {data!r}")</br>







## OUTPUT:
## Server Output : </br>
<img width="516" height="273" alt="Screenshot 2026-01-30 085219" src="https://github.com/user-attachments/assets/3f81a947-cc0a-4800-8f28-2eed9e00e43b" /></br>
## Client Output : </br>
<img width="479" height="254" alt="image" src="https://github.com/user-attachments/assets/b88eab02-c3fd-444b-beb1-7570ed33d79d" /></br>


## RESULT:
The program is executed successfully
