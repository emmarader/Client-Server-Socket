# importing header files
import socket
import logging


# creating a socket object
s = socket.socket()

print("Socket successfully created. Logfile: clientlog")

# verifying socket information
IP_address = input("\nEnter the server's external IP address: ")
client_port = input("\nEnter the server's port number: ")

# creating a client log
log = input("\nEnter filename to create a record of packets received: ")
logging.basicConfig(filename=log)

# initializing port number
port = 3389

# reading a message from user input
secret = input("\nEnter a message to send to the server: ")
print("\nSending Message to Server.")
print("\nThe message was sent to server: ", secret)

# connecting IP address and port number on server side to socket
s.bind(('', port))
print("\nSocket Binded to %s" %(port))

# socket is listening/waiting for connection
s.listen(5)
print("\nWaiting for Reply From Server...")

# create a condition because socket will always be waiting until force quit
while True:

     # connection with client side is made, socket is accepted on client side if addresses match
     c, addr = s.accept()

     print('\nReceived a Reply From Server. Hello', addr)

     # verify secret key word in communication
     if(secret == 'network'):
          print(secret, "is a good secret word")

     # close connection
     c.send('\nClosing Socket' .encode())
     c.close()
     break