FROM php:8.3-apache

RUN a2enmod rewrite

RUN apt-get update && apt-get install -y git unzip zip
RUN curl -sS https://get.symfony.com/cli/installer | bash
RUN mv /root/.symfony5/bin/symfony /usr/local/bin/symfony

## RUN git config --global user.email "{GITHUB_EMAIL_ADDRESS}"
## RUN git config --global user.name "{GITHUB_USERNAME}"

WORKDIR /var/www/html

COPY --from=mlocati/php-extension-installer /usr/bin/install-php-extensions /usr/local/bin/
RUN install-php-extensions gd pdo_mysql bcmath zip intl opcache

COPY --from=composer:2.1 /usr/bin/composer /usr/local/bin/composer