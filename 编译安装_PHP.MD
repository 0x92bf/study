#编译
##编译安装php所需的工具
```lib
sudo apt-get install \
build-essential \
gcc \
g++ \
autoconf \
libiconv-hook-dev \
libmcrypt-dev \
libxml2-dev \
libmysqlclient-dev \
libcurl4-openssl-dev \
libjpeg8-dev \
libpng-dev \
libfreetype6-dev \
libssl-dev \
libzip-dev
```
##编译安装PHP
```php
cd php/
./configure --prefix=/usr/local/php \
--with-config-file-path=/etc/php \
--enable-fpm \
--enable-pcntl \
--enable-mysqlnd \
--enable-opcache \
--enable-sockets \
--enable-sysvmsg \
--enable-sysvsem \
--enable-sysvshm \
--enable-shmop \
--enable-zip \
--enable-soap \
--enable-xml \
--enable-mbstring \
--disable-rpath \
--disable-debug \
--disable-fileinfo \
--with-mysqli=mysqlnd \
--with-pdo-mysql=mysqlnd \
--with-pcre-regex \
--with-iconv \
--with-zlib \
--with-gd \
--with-openssl \
--with-mhash \
--with-xmlrpc \
--with-curl \
--with-imap-ssl \
--with-bcmath

sudo make
sudo make install
sudo mkdir /etc/php
sudo cp php.ini-development /etc/php/php.ini
```
##设置php环境变量
1. ``vim ~/.bashrc``
2. 在文本末尾添加 ``export PATH=/usr/local/php/bin:$PATH
 export PATH=/usr/local/php/sbin:$PATH``
3. ``source ~/.bashrc``