# Level 3 – Task 1: Docker Swarm

## Step 1: Initialize Swarm
docker swarm init

## Step 2: Add Worker Nodes
docker swarm join --token <token> <manager_ip>:2377

## Step 3: Deploy a Service
docker service create --name web --replicas 3 -p 8080:80 nginx:latest

## Step 4: Verify Services
docker service ls
docker service ps web

## Step 5: Scale Services
docker service scale web=5

## Step 6: Remove Services
docker service rm web

## Step 7: Leave Swarm
docker swarm leave --force

