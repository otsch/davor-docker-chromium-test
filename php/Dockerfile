FROM php:8.2-fpm

ARG PHP_INI_ENVIRONMENT

# Install chromium
RUN apt-get update && apt-get install -y chromium

# Install node.js
#RUN curl -sL https://deb.nodesource.com/setup_16.x -o nodesource_setup.sh
#
#RUN bash nodesource_setup.sh
#
#RUN apt-get update && apt-get install -y nodejs build-essential

# Get default config for environment
RUN mv "$PHP_INI_DIR/php.ini-${PHP_INI_ENVIRONMENT}" "$PHP_INI_DIR/php.ini"

# Start php-fpm
CMD ["php-fpm"]
