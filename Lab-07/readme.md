# Lab 07 - Docker Compose - React + Node + MySql

## Build and run the app

1. Build the app

    `docker compose build`

2. Run the app

    `docker compose up -d`

    > This will take a while. When the app is running, launch the app in your browser http://localhost:3000

3. List the containers

    `docker compose ps`

4. Look at the backend container logs

    `docker compose logs -f backend`

5. Refresh the frontend page a few times, the logs should display each hit

6. Stop the app

    `docker compose down`

7. List the containers

    `docker compose ps`