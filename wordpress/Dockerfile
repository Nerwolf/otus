FROM wordpress:php8.1-fpm
RUN echo "pm.status_path = /status" >> /usr/local/etc/php-fpm.d/zz-docker.conf \
    && echo "ping.path = /ping" >> /usr/local/etc/php-fpm.d/zz-docker.conf.