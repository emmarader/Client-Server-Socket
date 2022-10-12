#README
Name: Emma Rader
Class: 4392
Section: 001

Project 1: CLient Server Socket Program

About: A client-side socket program to connect to a google cloud server

Prerequisites:
	- Latest version of python
	- an external IP address from a server

Libraries:
	- import socket // to create and close sockets
	- import logging // to keep a record of packets you received

Execution:

	1. Copy your external IP adress into line 4 of the client.py program
			ex: s.connect(('34.174.41.175', port))
	2. Open SSH on GCP
	3. Run python server.py
	4. Keep SSH window open but open your files on your computer and open client.py
	5. Server should be successfully connected


