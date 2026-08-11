01
Verify Docker Installation
Ensure Docker is installed and running before deploying the container.

Run these commands in your terminal

docker --version → confirms Docker is installed

systemctl status docker → checks Docker service status

02
Run Nginx Container
Core Command
Start the official Nginx image in detached mode and map it to port 8080.

Execute the run command

docker run -d -p 8080:80 nginx:latest

-d runs in detached mode

-p 8080:80 maps host port 8080 to container port 80

nginx:latest pulls the latest official Nginx image

03
Test in Browser
Confirm the container is serving the default Nginx page.

Open http://localhost:8080

You should see the default Nginx welcome page

04
Troubleshooting
Use Docker commands to inspect and manage the container if issues arise.

View logs: docker logs <container_id>

Stop container: docker stop <container_id>

Remove container: docker rm <container_id>

✅ Summary:

Task 1 was about building a custom Nginx container with your own index.html.

Task 2 is simpler: just run the official Nginx image and confirm it works.
