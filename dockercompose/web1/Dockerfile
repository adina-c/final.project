FROM php:7.0-apache

RUN apt-get update
RUN apt-get install -y git
RUN git clone https://github.com/banago/simple-php-website.git
RUN cp -r simple-php-website/* /var/www/html/

COPY home.phtml /var/www/html/content/home.phtml

RUN /bin/bash -c "a2enmod rewrite"

RUN /bin/bash -c "service apache2 restart"

EXPOSE 80

CMD apachectl -D FOREGROUND
