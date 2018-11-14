FROM ubuntu:latest

LABEL maintainer="FoodLogiQ <technology@foodlogiq.com>"

ENV CHROMEDRIVER_VERSION 2.38

RUN set -xe \
        \
        && apt-get update \
        \
        && apt-get install -y \
            gnupg \
            wget \
            curl \
        \
        && wget -q -O - https://dl-ssl.google.com/linux/linux_signing_key.pub | apt-key add - \
        \
        && echo "deb http://dl.google.com/linux/chrome/deb/ stable main" >> /etc/apt/sources.list.d/google.list \
        \
        && apt-get update \
        \
        && apt-get install -y \
            gcc \
            python \
            python-pip \
            unzip \
            libdbus-glib-1-dev \
            libgtk2.0-0 \
            google-chrome-stable \
        \
        && apt-get clean \
        \
        && apt-get autoremove

RUN curl -sSLO "https://chromedriver.storage.googleapis.com/$CHROMEDRIVER_VERSION/chromedriver_linux64.zip" \
        \
        && unzip "chromedriver_linux64.zip" -d /usr/local/bin \
        \
        && rm "chromedriver_linux64.zip" 