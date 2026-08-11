01 step‑by‑step instructions 
Verify Docker Installation
Ensure Docker is installed and running before building the image.

Run these commands in terminal

docker --version

systemctl status docker

02
Build the Image
Use the Dockerfile to build a custom Nginx image.

Execute in project root

Navigate to level1/nginx-container

Run docker build -t my-nginx ./level1/nginx-container

03
Run the Container
Start the container and map port 8080 to 80.

Run docker run -d -p 8080:80 my-nginx

Container runs in background

04
Test in Browser
Validation
Confirm the container is serving your custom page.

Open http://localhost:8080

Page should display 'Hello from Docker Nginx!'

05
Troubleshooting
Check logs and container status if issues occur.

Logs: docker logs <container_id>

Restart: docker restart <container_id>

Inspect: docker inspect <container_id>
