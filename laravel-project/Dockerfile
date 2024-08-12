FROM php:8.4.0alpha4-zts-bullseye

RUN apt-get update -y && apt-get install -y openssl zip unzip 

RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

WORKDIR /app

COPY . /app

RUN composer install

EXPOSE 8002

CMD php artisan serve --host=0.0.0.0 --port=8002