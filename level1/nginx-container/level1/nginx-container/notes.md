# Level 1 – Deploy Nginx Container

## Step 1: Verify Docker Installation
```bash
docker --version
systemctl status docker

Step 2: Build the Image
docker build -t my-nginx ./level1/nginx-container

Step 3: Run the Container
docker run -d -p 8080:80 my-nginx

Step 4: Test in Browser
Open: http://localhost:8080

Step 5: Troubleshooting
Logs: docker logs <container_id>

Restart: docker restart <container_id>

Inspect: docker inspect <container_id>
