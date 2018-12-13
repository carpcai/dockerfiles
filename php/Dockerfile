FROM php:7.2

# constant
ARG COMPOSER=https://getcomposer.org/installer
ARG COMPOSER_ADDR=https://packagist.phpcomposer.com

# Install composer
RUN curl -sS ${COMPOSER} | php; \
	mv composer.phar /usr/local/bin/composer; \
	chmod +x /usr/local/bin/composer; \
	composer -V; \
	if [ ${COMPOSER_ADDR} ]; then \
		composer config -g repo.packagist composer ${COMPOSER_ADDR}; \
	fi


