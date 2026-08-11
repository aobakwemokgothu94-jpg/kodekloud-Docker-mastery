# Level 1 – Task 5: Troubleshoot Container

## Step 1: Check Running Containers
docker ps

## Step 2: View Logs
docker logs <container_id>

## Step 3: Inspect Container Details
docker inspect <container_id>

## Step 4: Restart Container
docker restart <container_id>

## Step 5: Access Container Shell (if needed)
docker exec -it <container_id> /bin/bash

## Step 6: Verify Container Health
- Check if the application is responding on its mapped port
- Use curl or browser: curl http://localhost:<mapped_port>
