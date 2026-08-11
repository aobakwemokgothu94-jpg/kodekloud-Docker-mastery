# Level 1 – Task 2: Deploy Nginx Container

## Step 1: Verify Docker Installation
docker --version
systemctl status docker

## Step 2: Run Nginx Container
docker run -d -p 8080:80 nginx:latest

- -d → run in detached mode
- -p 8080:80 → map host port 8080 to container port 80
- nginx:latest → pull and run the official Nginx image

## Step 3: Test in Browser
Open: http://localhost:8080  
You should see the default Nginx welcome page.

## Step 4: Troubleshooting
- Logs: docker logs <container_id>
- Stop container: docker stop <container_id>
- Remove container: docker rm <container_id>
