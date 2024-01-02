FROM python:3.7-alpine3.8

LABEL maintainer="FoodLogiQ <technology@esha.com>"

RUN echo "http://dl-4.alpinelinux.org/alpine/v3.8/main" >> /etc/apk/repositories \
        && echo "http://dl-4.alpinelinux.org/alpine/v3.8/community" >> /etc/apk/repositories \
        && apk update \
        && apk add \
            chromium \
            chromium-chromedriver