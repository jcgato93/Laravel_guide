FROM php:7.2-apache

RUN apt-get update

# Install some utils
# RUN apt-get install -y \
#     curl \
#     git \
#     supervisor \
#     unzip \
#     vim

# PHP ext
RUN apt-get install -y libpq-dev \
    && docker-php-ext-configure pgsql -with-pgsql=/usr/local/pgsql \
    && docker-php-ext-install pdo pdo_pgsql pgsql

# COPY --from=latest /usr/bin/composer /usr/bin/composer

# For mysql
# RUN apt-get update && apt-get install -y \
#     && docker-php-ext-install mysqli pdo pdo_mysql


RUN a2enmod rewrite

RUN chmod 777 -R -c /var/www
