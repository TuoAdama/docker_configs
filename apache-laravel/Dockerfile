FROM oberd/php-8.0-apache
COPY laravel.conf /etc/apache2/sites-available
RUN a2dissite 000-default.conf && a2ensite laravel.conf
RUN service apache2 restart
EXPOSE 80