# Level 3 – Task 4: Docker Registry

## Step 1: Run Private Registry
docker run -d -p 5000:5000 --name registry registry:2

## Step 2: Tag Image
docker tag nginx:latest localhost:5000/mynginx

## Step 3: Push Image
docker push localhost:5000/mynginx

## Step 4: Pull Image
docker pull localhost:5000/mynginx

## Step 5: Authentication
docker login localhost:5000

