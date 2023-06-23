FROM ubuntu:latest

# Install NGINX and additional packages
RUN apt-get update && \
    apt-get install -y \
    nginx \
    nano \
    curl \
    && apt-get clean

# Remove default NGINX configuration
RUN rm /etc/nginx/sites-enabled/default

# Copy custom NGINX configuration
# COPY nginx.conf /etc/nginx/nginx.conf

# Copy website files
# COPY index.html /var/www/html/index.html

# Expose ports
EXPOSE 80

# Start NGINX service
CMD ["nginx", "-g", "daemon off;"]