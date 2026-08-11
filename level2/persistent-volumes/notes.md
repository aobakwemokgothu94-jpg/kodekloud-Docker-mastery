# Level 2 – Task 2: Persistent Volumes

## Step 1: Create a Volume
docker volume create my_volume

## Step 2: Run a Container with the Volume
docker run -d --name mydb -v my_volume:/var/lib/mysql mysql:latest

- -v my_volume:/var/lib/mysql → mounts the volume to MySQL data directory
- Data stored here will persist even if the container is deleted

## Step 3: Verify Volume Exists
docker volume ls

## Step 4: Inspect Volume Details
docker volume inspect my_volume

## Step 5: Test Persistence
- Stop and remove the container:
  docker stop mydb
  docker rm mydb
- Run a new container with the same volume:
  docker run -d --name mydb2 -v my_volume:/var/lib/mysql mysql:latest
- The data remains intact because it’s stored in the volume.

