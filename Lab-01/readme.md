# Lab 01 - Run your first container

### Pull and run Nginx
docker run -d -p 8080:80 --name webserver nginx

### List the running containers
docker ps

### List the images
docker images

### Attach to the container
docker container exec -it webserver bash  

### Inspect the OS version
cat /etc/os-release

### Exit the shell
exit

### Stop the container
docker container stop webserver

### List all containers
docker ps --all

### Remove the container from memory
docker container rm webserver

### Remove the image
docker image rm nginx