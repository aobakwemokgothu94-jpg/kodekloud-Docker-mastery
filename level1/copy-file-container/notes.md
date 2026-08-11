# Level 1 – Task 4: Copy File into Container

## Step 1: Identify the Running Container
docker ps

## Step 2: Copy a File into the Container
docker cp <local_file_path> <container_id>:/path/in/container/

Example:
docker cp sample.txt <container_id>:/usr/share/nginx/html/

## Step 3: Verify the File Inside the Container
docker exec -it <container_id> ls /usr/share/nginx/html/

## Step 4: Optional – View File Content
docker exec -it <container_id> cat /usr/share/nginx/html/sample.txt
