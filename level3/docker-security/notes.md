# Level 3 – Task 2: Docker Security

## Step 1: Run as Non-Root
FROM nginx:latest
RUN adduser --disabled-password myuser
USER myuser

## Step 2: Limit Capabilities
docker run --cap-drop=ALL --cap-add=NET_BIND_SERVICE nginx:latest

## Step 3: Read-Only Filesystem
docker run -d --name secure-nginx --read-only -p 8080:80 nginx:latest

## Step 4: Scan Images
docker scan nginx:latest

## Step 5: Secrets Management
echo "mypassword" | docker secret create db_pass -

## Step 6: Network Isolation
- Use custom networks
- Only expose required ports

