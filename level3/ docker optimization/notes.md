# Level 3 – Task 3: Docker Optimization

## Step 1: Multi-Stage Builds
FROM golang:1.20 AS builder
WORKDIR /app
COPY . .
RUN go build -o myapp

FROM alpine:latest
COPY --from=builder /app/myapp /myapp
CMD ["./myapp"]

## Step 2: Resource Limits
docker run -d --cpus=1 --memory=512m nginx:latest

## Step 3: Layer Caching
- Order Dockerfile instructions to maximize cache reuse
- Avoid unnecessary rebuilds

## Step 4: Use Smaller Base Images
- Prefer alpine or scratch

