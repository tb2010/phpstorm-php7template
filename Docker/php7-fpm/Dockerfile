FROM php:8
RUN apt-get update \
 && apt-get install -y \
      libpq-dev \
      libmcrypt-dev \
      libpng12-dev \
      libfreetype6-dev \
      libjpeg62-turbo-dev \
 && docker-php-ext-install iconv mcryptd pdo pdo_pgsql pdo_mysql

 COPY build/app  /var/www

 EXPOSE 80 443
 VOLUME /var/www
 VOLUME /var/log

 RUN apt-get clean && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
