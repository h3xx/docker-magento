FROM markoshust/magento-php:7.4-fpm-14

USER root

RUN pecl install oauth && \
	rm -rf /tmp/pear
RUN docker-php-ext-enable oauth

USER app
