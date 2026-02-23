Introduction to Docker
-------------------------------

Docker:-
Docker is a tool used to create and run containers.
It helps developers run applications the same way on every machine.

Container:-
A container is a small package that includes:
Application code
Required libraries
Dependencies
Runtime
It contains everything needed to run the application.

Architecture:-
Docker has 5 main parts:
Docker Client
Docker Daemon
Docker Image
Docker Container
Docker Registry
----------------------------------------------
Install Docker
command:- sudo apt update
          sudo apt install docker.io 
          sudo systemctl start docker
          docker --version
          docker run hello-world
________________________________________________
Run Containers
Run Nginx
command:- docker run -d -p 8080:80 nginx
Run an Ubuntu container in interactive mode :- docker run -it ubuntu

List Containers:- docker ps
All containers:- docker ps -a
Stop Container:- docker stop container_id
Remove Container :- docker rm container_id
-----------------------------------------------------
Explore
Runs in background :- docker run -d nginx
Give Name to Container :- docker run -d --name myapp nginx
Port Mapping :- docker run -d -p 3000:80 nginx
Check Logs :- docker logs myapp
Run Inside Container :- docker exec -it myapp bash

