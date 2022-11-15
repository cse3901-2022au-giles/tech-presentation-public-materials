## Simple Client-Server TCP Connection Demo (Python) (Shredder)
### TCP Server
```
import socket
import sys

ip = "127.0.0.1"
port = 5432
address = (ip,port)

server = socket.socket(socket.AF_INET, socket.SOCK_STREAM)
server.bind((ip, port))
server.listen(5)

print ("Listening on ", address)

def handle_client(client_socket):
    request = client_socket.recv(1024)
    print ("Received: ", request)
    client_socket.send("Received!")
    client_socket.close()
while True:
    client, addr = server.accept()
    print ("Accepted connection from: ", addr[0], addr[1])
    client.start()
```

### TCP Client
```
import socket
import sys

ip = "127.0.0.1"
port = 5432
address = (ip,port)

client = socket.socket(socket.AF_INET, socket.SOCK_STREAM)
client.connect(address)
client.send("Send!")
response = client.recv(2048)

print response
```
