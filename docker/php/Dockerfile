FROM php:8.1-fpm

RUN apt update && apt install -y zlib1g-dev libpng-dev && rm -rf /var/lib/apt/lists/*

RUN docker-php-ext-install gd
RUN docker-php-ext-install mysqli
#RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer
COPY --from=composer:2.5.7 /usr/bin/composer /usr/bin/composer