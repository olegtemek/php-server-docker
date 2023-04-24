FROM php:8.1-fpm
# FROM php:7.4-fpm

RUN apt-get update \
  && docker-php-ext-install pdo pdo_mysql

# INSTALL COMPOSER
RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

# OTHER REQUIREMENTS
RUN apt-get install -y p7zip \
  p7zip-full \
  unace \
  zip \
  unzip \
  xz-utils \
  sharutils \
  uudeview \
  mpack \
  arj \
  cabextract \
  file-roller \
  && rm -rf /var/lib/apt/lists/*


# # !OPENCART

# WORKDIR /var/www/app

# RUN apt-get install -y \
#   libzip-dev \
#   zip \
#   && docker-php-ext-install zip

# # Setup GD extension
# RUN apt-get install -y libfreetype6-dev libjpeg62-turbo-dev libpng-dev && \
#   docker-php-ext-configure gd --with-freetype=/usr/include/ --with-jpeg=/usr/include/ && \
#   docker-php-ext-install gd

# # !OPENCART