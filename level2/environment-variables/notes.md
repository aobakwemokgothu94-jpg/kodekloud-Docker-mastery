# Level 2 – Task 4: Environment Variables

## Step 1: Run a Container with Environment Variables
docker run -d --name mydb \
  -e MYSQL_ROOT_PASSWORD=rootpass \
  -e MYSQL_DATABASE=mydb \
  mysql:latest

- -e → sets environment variables inside the container
- MYSQL_ROOT_PASSWORD → sets the root password
- MYSQL_DATABASE → creates a database at startup

## Step 2: Verify Environment Variables
docker exec -it mydb env

## Step 3: Use Environment Variables in Docker Compose
Example docker-compose.yml snippet:

version: '3.8'
services:
  db:
    image: mysql:latest
    environment:
      MYSQL_ROOT_PASSWORD: rootpass
      MYSQL_DATABASE: mydb

## Step 4: Externalize Environment Variables
- Create a `.env` file:
  MYSQL_ROOT_PASSWORD=rootpass
  MYSQL_DATABASE=mydb

- Reference it in docker-compose.yml:
  env_file:
    - .env

## Step 5: Benefits
- Securely manage secrets and configs
- Easily change values without editing Dockerfiles
- Reuse across multiple environments (dev, test, prod)

