# Use the official PHP image as the base image
FROM php:7.4-apache

# Set the working directory
WORKDIR /var/www/html

# Install PHP extensions
RUN docker-php-ext-install pdo pdo_mysql zip

# Enable Apache mod_rewrite
RUN a2enmod rewrite

# Install Composer
RUN apt-get update && apt-get install -y \
    git \
    zip \
    unzip

# Download and install Composer
RUN php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');"
RUN php composer-setup.php --install-dir=/usr/local/bin --filename=composer

# Remove the Composer setup files
RUN php -r "unlink('composer-setup.php');"

# Copy the backend files
COPY . .

# Check if composer.json exists, and if so, install dependencies
RUN if [ -f "composer.json" ]; then composer install; fi

# Set permissions for storage and bootstrap/cache folders
RUN chown -R www-data:www-data storage bootstrap/cache

# Expose port 80
EXPOSE 80

# Start Apache
CMD ["apache2-foreground"]
