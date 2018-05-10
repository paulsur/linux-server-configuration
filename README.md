## Linux Server Configuration Project

### Description
This project deployed the previous catalog flask application onto a virtual Ubuntu linux server on Amazon Lightsail

### Access
The webpage can be accessed at:
http://52.89.247.95.xip.io/

The server can be accessed through SSH at IP 52.89.247.95, port 2200, user grader. To access save the private key (included in project submission) to ~/.ssh/linuxCourse and run:
```
ssh grader@52.89.247.95 -p 2200 -i ~/.ssh/linuxCourse
```

Once logged in through SSH the files can be found in /home/grader/catalog

The Github page with the README.md file is at:

https://github.com/paulsur/linux-server-configuration

### Software configuration
1. The Ubuntu machine software was updated and upgraded to be the most recent version 
2. Python 3, I am using version 3.5.2
	1. Needed to install pip3 (python3-pip) module. Ignore the warnings about the latest version needing to be installed as it breaks the configuration.
3. PostgreSQL for the database server
	1. Uses the "catalog" user and database for the web app
4. Apache2 and WSGI are used to serve the web app
5. Configured firewall through UFW to only allow incoming connections on ports 80, 123, and 2200

### Database Initialization
The database should be initialized, if the database doesn't exist, from the command prompt using:
```
python database_setup.py
```

### Sources
Using python version 3+ introduced some additional errors that required using Google and Stack Overflow to find the answers.
