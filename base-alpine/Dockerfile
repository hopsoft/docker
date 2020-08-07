from ruby:2.7.1-alpine

RUN apk add --update nodejs npm yarn alpine-sdk zsh sqlite sqlite-dev tzdata
RUN gem install rails 
RUN rails webpacker:install
