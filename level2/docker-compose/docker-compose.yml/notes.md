📌 docker-compose.yml (example setup)
yaml

version: '3.8'

services:
  web:
    image: nginx:latest
    ports:
      - "8080:80"
    networks:
      - my_network

  redis:
    image: redis:latest
    networks:
      - my_network

  db:
    image: mysql:latest
    environment:
      MYSQL_ROOT_PASSWORD: rootpass
      MYSQL_DATABASE: mydb
    volumes:
      - db_data:/var/lib/mysql
    networks:
      - my_network

networks:
  my_network:

volumes:
  db_data:

📌 notes.md Content

# Level 2 – Task 3: Multi-Container Setup with Docker Compose

## Step 1: Create docker-compose.yml
Define multiple services (web, redis, db) in one file.

## Step 2: Start Containers
docker-compose up -d

## Step 3: Verify Running Services
docker-compose ps

## Step 4: Test Connectivity
- Access Nginx: http://localhost:8080
- Redis and MySQL run internally on the same network.

## Step 5: Stop and Remove Containers
docker-compose down

## Step 6: Persist Data
- MySQL data is stored in the named volume `db_data`.
- Data remains even after containers are removed.
