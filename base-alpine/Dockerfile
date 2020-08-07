from ruby:2.7.1-alpine

RUN apk add --update nodejs npm yarn alpine-sdk zsh sqlite sqlite-dev tzdata libpq postgresql-dev



# establish the working directory for the current project
WORKDIR /application
COPY . /application/

# configure and install rails 
#RUN bundle install rails 
RUN bundle install
RUN rails webpacker:install

CMD rails s -b 0.0.0.0
