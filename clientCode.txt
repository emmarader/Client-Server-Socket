# importing header files
import socket

# create socket object on client side
s = socket.socket()

# initialize port number
port = 3389

# connect external IP address and port number of server to socket
s.connect(('34.174.41.175', port))

# print confirmation message

print(s.recv(1024).decode())

# close socket
s.close()
