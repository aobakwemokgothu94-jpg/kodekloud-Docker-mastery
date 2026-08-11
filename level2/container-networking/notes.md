# Level 2 – Task 1: Container Networking

## Step 1: Create a Custom Network
docker network create my_network

## Step 2: Run First Container (Nginx)
docker run -d --name web --network my_network -p 8080:80 nginx:latest

## Step 3: Run Second Container (BusyBox or Alpine)
docker run -it --name test --network my_network busybox

## Step 4: Verify Connectivity
Inside the "test" container:
ping web
wget -qO- http://web

## Step 5: List Networks
docker network ls

## Step 6: Inspect Network
docker network inspect my_network

