FROM phpdockerio/php80-fpm:latest
WORKDIR "/application"

LABEL maintainer="Humphrey Ndirangu"

# Fix debconf warnings upon build
ARG DEBIAN_FRONTEND=noninteractive

# Install extensions and clean system
RUN apt-get update \
    && apt-get -y --no-install-recommends install php8.0-mysql libmcrypt-dev \
    && apt-get clean; rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* /usr/share/doc/*

# Install git
RUN apt-get update \
    && apt-get -y install git \
    && apt-get clean; rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* /usr/share/doc/*