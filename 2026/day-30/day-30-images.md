Docker Images & Container Lifecycle
-----------------------------------------

Pull Images from Docker Hub :- docker pull nginx
                               docker pull ubuntu
                               docker pull alpine

Compare ubuntu vs alpine — why is one much smaller?
Ubuntu :- Full Linux distribution
          Many packages included
Alpine :- Minimal Linux distribution
          Only basic tools
          Designed for containers         

List All Images :- docker images
  docker inspect nginx

Remove an Image  :- docker rmi alpine
------------------------------------------------

Image Layers
Check Image History :- docker image history nginx

What Are Layers?
Layers are small parts of an image.
Each Docker command (FROM, RUN, COPY) creates a new layer.
Example:
Base OS layer
Install packages layer
Copy files layer

Why Does Docker Use Layers?
Faster builds
Saves space (layers are reused)
Easy caching
Easy updates

---------------------------------------------------

understand how images and containers actually work

Create Container :- docker create --name myubuntu ubuntu
Start Container :- docker start myubuntu
Pause Container :- docker pause myubuntu
Unpause         :- docker unpause myubuntu
Stop Container :- docker stop myubuntu
Restart Container :- docker restart myubuntu
Kill Container    :- docker kill myubuntu
Remove Container :- docker rm myubuntu

Working with Running Containers

Run Nginx in Detached Mode :-  docker run -d --name mynginx -p 8080:80 nginx
View Logs :- docker logs mynginx
Real-Time Logs (follow mode) :- docker logs -f mynginx
Exec Into Container :- docker exec -it mynginx bash
Run Single Command Without Entering :- docker exec mynginx ls /
Inspect Container :- docker inspect mynginx

________________________________________________

Cleanup
Stop All Running Containers :- docker stop $(docker ps -q)
Remove All Stopped Containers :- docker rm $(docker ps -aq)
Remove Unused Images :- docker image prune (prune means Remove unused or unnecessary Docker data.)
Check Docker Disk Usage :- docker system df 

