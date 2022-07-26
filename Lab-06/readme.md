# Lab 06 - Docker Compose

## Build the application

1. Build the application by running `docker compose build`

2. Run the app

    `docker compose up -d`

    > When the app runs, launch the voting app in your browser http://localhost:5000

3. List the containers

    `docker compose ps`

4. Look at the container logs
   
   `docker compose logs -f web-fe`

5. List the current projects

    `docker compose ls`

6. Let’s try to deploy a second version

    `docker compose up -d`

    > This fails because we can only run an app a single time.  Deploy a second version using a different project name

7. Let’s now use a project name to see if we can deploy a second version
    
    `docker compose -p test up -d`

    > This fails because the localhost port 5000 is already assigned.

8. Change the ports value from "5000:80" to "5001:80"

9. Deploy again

    `docker compose -p test up -d`

10. List all running compose projects

    `docker compose ls`

## Cleanup

```
docker compose down
docker compose ls
docker compose -p test down
docker compose ls
```