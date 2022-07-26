# Lab 02 - Build a custom image

### Create a Dockerfile
- Create a new file and name it Dockerfile (without any file extension).
- Add the following content in the newly created Dockerfile and save it:

```
FROM nginx:alpine
COPY index.html /usr/share/nginx/html

```

### Create the index.html file
- Create a new file and name it index.html
- Add the following content:

```
<html>
    <head></head>
    <body>
        <h1>Hello World!</h1>
    </body>
</html>
```

### Build the image
docker build -t hello-world:v1 .

### List the images
docker images

### Run the container
docker run -d -p 8080:80 --name hello hello-world:v1

### List the running containers
docker ps

### Display the page with cURL
curl localhost:8080

> You can also use your browser to navigate to the page.

### Stop the container

docker stop hello

> Refresh the browser to confirm that it has stopped.

### List the running containers 

docker ps

> You should not see the hello-world:v1 instance anymore.

### Remove the instance from memory
docker container rm hello

### Confirm that the container is no longer running
docker ps --all

### List the images
docker images

### Delete the image
docker image rm hello-world:v1