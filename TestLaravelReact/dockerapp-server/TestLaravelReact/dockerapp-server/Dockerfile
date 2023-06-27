# Use the official PHP image with FPM (FastCGI Process Manager) as the base image
FROM php:8.1-fpm

# Set the working directory in the container
WORKDIR /var/www/html

# Copy the project files and directories to the container
COPY . .

# Install PHP dependencies using Composer
RUN apt-get update && apt-get install -y \
    zip \
    unzip \
    libonig-dev \
    libxml2-dev \
    nano \
    && docker-php-ext-install pdo_mysql mbstring exif pcntl bcmath \
    && curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

# Install Laravel dependencies
RUN composer install --optimize-autoloader --no-dev

# Set the proper permissions
RUN chown -R www-data:www-data /var/www/html/storage /var/www/html/bootstrap/cache

# Remove the default Nginx configuration
RUN rm /etc/nginx/conf.d/default.conf

# Copy your custom Nginx configuration file
COPY nginx.conf /etc/nginx/conf.d

# Expose port 80
EXPOSE 80

# Start PHP-FPM and Nginx
CMD ["sh", "-c", "service php8.1-fpm start && nginx -g 'daemon off;'"]
