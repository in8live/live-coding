FROM php:8.2-fpm

RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

RUN set -xe; \
    apt-get update -yqq && \
    apt-get install -y apt-utils libzip-dev zip unzip && \
    apt-get install -y --no-install-recommends openssl libssl-dev libcurl4-openssl-dev libicu-dev libgmp-dev \
      libfreetype6-dev libjpeg62-turbo-dev libpng-dev

RUN set -uex; \
    apt-get update; \
    apt-get install -y ca-certificates curl gnupg; \
    mkdir -p /etc/apt/keyrings; \
    curl -fsSL https://deb.nodesource.com/gpgkey/nodesource-repo.gpg.key \
     | gpg --dearmor -o /etc/apt/keyrings/nodesource.gpg; \
    NODE_MAJOR=18; \
    echo "deb [signed-by=/etc/apt/keyrings/nodesource.gpg] https://deb.nodesource.com/node_$NODE_MAJOR.x nodistro main" \
     > /etc/apt/sources.list.d/nodesource.list; \
    apt-get update; \
    apt-get install nodejs -y

RUN apt-get update && apt-get install -y \
    && docker-php-ext-install pdo pdo_mysql mysqli zip pcntl sockets intl gmp gd

RUN apt-get install -y vim-nox git
