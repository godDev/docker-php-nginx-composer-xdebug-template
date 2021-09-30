FROM phpdockerio/php80-fpm:latest
WORKDIR "/var/www/application"

RUN mkdir /var/www/.composer && chown www-data /var/www/.composer
COPY --from=composer:latest /usr/bin/composer /usr/bin/composer

RUN apt-get update; \
    apt-get -y --no-install-recommends install \
        php8.0-xdebug; \
    apt-get clean; \
    rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* /usr/share/doc/*
