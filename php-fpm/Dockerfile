FROM alpine:3.4

MAINTAINER Vincent Composieux <vincent.composieux@gmail.com>

RUN apk add --update \
    php5-fpm \
    php5-apcu \
    php5-curl \
    php5-gd \
    php5-iconv \
    php5-imagick \
    php5-json \
    php5-intl \
    php5-mcrypt \
    php5-mysql \
    php5-opcache \
    php5-openssl \
    php5-pdo \
    php5-pdo_mysql \
    php5-mysqli \
    php5-xml \
    php5-dom \
    php5-ctype \
    php5-zlib

RUN rm -rf /var/cache/apk/* && rm -rf /tmp/*

ADD symfony.ini /etc/php5/fpm/conf.d/
ADD symfony.ini /etc/php5/cli/conf.d/

ADD symfony.pool.conf /etc/php5/fpm.d/

CMD ["php-fpm", "-F"]

EXPOSE 9000
