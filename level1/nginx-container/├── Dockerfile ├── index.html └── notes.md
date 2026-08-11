# Use the official Nginx image as base
FROM nginx:latest

# Copy a custom index.html into the container
COPY ./index.html /usr/share/nginx/html/index.html

# Expose port 80 for web traffic
EXPOSE 80
