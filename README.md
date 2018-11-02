# Docker
TO Get Image
docker pull nginx


To See the port (Exposed port)
docker inspect nginx






To see the installed Images
docker images 


To publish the exposed port 80 as 8080
//detach will run the container in the background
docker run -p 8080:80 --detach nginx






To see running container
docker ps


go to local host and press port 8080




when you install docker for first time it will install three networks
docker network ls


which network your container can talk to by default connect to bridge
docker network inspect bridge


Stop the container
docker stop containerID 
docker ps




chekc the container array it should be empty
docker network inspect bridge 






Pull ubuntu
docker pull ubuntu


change the name to container 2 
docker run -it --detach --name=container2 ubuntu


Since both containers are running we can see them in network inspect
docker network inspect bridge
NOTE: if you try to contact the IPv4 from the local via ping ipppppp
It will not be accessable by the local but they are accessable among the containers.


docker attach container1
ping 172.17.0.3
Error: Ping command not found
>Install the ping command via 
apt-get update 
apt-get install iputils-ping


// Now you can see that pings work


TO exist on shell in container 2 and back to host OS
exit


To stop container
docker stop container2
doc
docker network inspect bridge
