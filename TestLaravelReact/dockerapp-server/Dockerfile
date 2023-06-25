# Use the official PHP image with Apache as the base image
FROM php:8.1-apache

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

# Enable Apache rewrite module
RUN a2enmod rewrite

# Expose port 80
EXPOSE 80

# Start the Apache server
CMD ["apache2-foreground"]
