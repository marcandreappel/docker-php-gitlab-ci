FROM ubuntu:20.04
ENV DEBIAN_FRONTEND noninteractive
RUN apt update && \
    apt install -y software-properties-common && \
    add-apt-repository -y ppa:ondrej/php && \
    apt install -y curl git php8.0-json php8.0-curl php8.0-gd \
    php8.0-intl php8.0-mbstring php8.0-cli php8.0-zip php8.0-xsl \
    php8.0-phar php8.0-xml php8.0-bcmath php8.0-sqlite3 \
    php-xdebug
RUN php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');" && \
    php -r "if (hash_file('sha384', 'composer-setup.php') === '756890a4488ce9024fc62c56153228907f1545c228516cbf63f885e036d37e9a59d27d63f46af1d4d07ee0f76181c7d3') { echo 'Installer verified'; } else { echo 'Installer corrupt'; unlink('composer-setup.php'); } echo PHP_EOL;" && \
    php composer-setup.php && \
    php -r "unlink('composer-setup.php');" && \
    mv composer.phar /usr/local/bin/composer
