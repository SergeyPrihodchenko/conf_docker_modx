FROM phpdockerio/php:8.2-fpm
WORKDIR "/application"

COPY . /application

RUN apt-get update \
    && apt-get -y --no-install-recommends install \
        php8.2-mysql \
        php8.2-gd \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* /usr/share/doc/*

# RUN chown -R www-data:www-data /application

# RUN /usr/bin/mysql -u dev -h localhost -P 3306 -p DB < dk-lok.sql \ 123 \