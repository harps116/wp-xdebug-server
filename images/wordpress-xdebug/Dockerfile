
FROM wordpress

RUN apt-get update
RUN apt-get install -y apt-utils vim wget git subversion
RUN cd
RUN wget https://phar.phpunit.de/phpunit-6.1.phar -P /opt/
RUN chmod +x /opt/phpunit-6.1.phar
RUN mv /opt/phpunit-6.1.phar /usr/local/bin/phpunit
RUN phpunit --version
RUN wget https://raw.githubusercontent.com/wp-cli/builds/gh-pages/phar/wp-cli.phar -P /opt/
RUN chmod +x /opt/wp-cli.phar
RUN mv /opt/wp-cli.phar /usr/local/bin/wp
RUN wp --info
RUN pecl install xdebug


EXPOSE 80
