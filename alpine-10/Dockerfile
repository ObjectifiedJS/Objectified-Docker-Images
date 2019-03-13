FROM node:10-alpine

LABEL organization="ObjectifiedJS https://github.com/ObjectifiedJS"

RUN \
  echo "http://dl-cdn.alpinelinux.org/alpine/edge/community" >> /etc/apk/repositories \
  && echo "http://dl-cdn.alpinelinux.org/alpine/edge/main" >> /etc/apk/repositories \
  && apk --no-cache update \
  && apk --no-cache upgrade \
  && apk add --no-cache --virtual .build-deps udev ttf-opensans chromium firefox \
  && rm -rf /var/cache/apk/* /tmp/*

ENV CHROME_BIN /usr/bin/chromium-browser
ENV FIREFOX_BIN /usr/bin/firefox-browser
