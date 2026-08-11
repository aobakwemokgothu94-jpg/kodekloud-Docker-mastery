# Level 4 – Task 1: Kubernetes Integration

## Step 1: Deploy Docker Image to Kubernetes
kubectl run myapp --image=nginx:latest --port=80

## Step 2: Expose Deployment
kubectl expose deployment myapp --type=NodePort --port=80

## Step 3: Verify Pods
kubectl get pods

## Step 4: Scale Deployment
kubectl scale deployment myapp --replicas=3

## Step 5: Apply YAML Manifest
kubectl apply -f deployment.yaml

