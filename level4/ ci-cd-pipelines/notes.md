# Level 4 – Task 3: CI/CD Pipelines

## Step 1: Build Image in Pipeline
docker build -t myapp:latest .

## Step 2: Push to Registry
docker push myregistry/myapp:latest

## Step 3: Deploy Automatically
kubectl apply -f deployment.yaml

## Step 4: Example GitHub Actions Workflow
name: CI/CD
on: [push]
jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
      - run: docker build -t myapp:latest .
      - run: docker push myregistry/myapp:latest
      - run: kubectl apply -f deployment.yaml

