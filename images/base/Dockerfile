FROM ubuntu:18.04
RUN apt update && \
  apt install -y software-properties-common && \
  add-apt-repository -y ppa:ondrej/php && \
  apt install -y curl git php7.4-json php7.4-curl \
    php7.4-intl php7.4-mbstring php7.4-cli php7.4-zip \
    php7.4-phar php7.4-xml php-xdebug composer
    
