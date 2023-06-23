# Use the official Ubuntu base image
FROM ubuntu:latest

# Set the working directory inside the container
WORKDIR /app

# Update the package lists and install necessary packages
RUN apt-get update && \
    apt-get install -y \
    nginx \
    nano \
    curl \
    && apt-get clean

# Copy Nginx configuration
COPY nginx.conf /etc/nginx/nginx.conf

# Expose ports
EXPOSE 80

# Start Nginx service
CMD ["nginx", "-g", "daemon off;"]