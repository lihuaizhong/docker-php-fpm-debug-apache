# 使用官方 PHP-FPM 镜像
FROM php:8.2-fpm

# 安装 Xdebug
RUN pecl install xdebug \
    && docker-php-ext-enable xdebug 

# 配置 Xdebug
#COPY xdebug.ini /usr/local/etc/php/conf.d/xdebug.ini
RUN apt update && \
    apt install -y net-tools vim && \
    apt clean && \
    rm -rf /var/lib/apt/lists/*
WORKDIR /var/www/html