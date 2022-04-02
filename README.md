# client.py
#ryp-01
import socket
IP= socket.gethostbyname(socket.gethostname())
PORT=8000
HEADER=1024

client=socket.socket()
client.connect((IP,PORT))
print(f"[CONNECTED]conectado al servidor en {IP}")

while True:
    msg=input("Ingrese un mensaje:")
    encoded=msg.encode("utf-8")
    client.send(encoded)
