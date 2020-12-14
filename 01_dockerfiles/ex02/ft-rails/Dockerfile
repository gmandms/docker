FROM ruby:latest
MAINTAINER sbump <sbump@student.21-school.ru>

RUN apt-get update -y && \
		apt-get upgrade -y && \
		apt-get install -y nodejs sqlite3

RUN gem install bundler rails

ONBUILD COPY app /opt/app
ONBUILD WORKDIR /opt/app

ONBUILD EXPOSE 3000
ONBUILD RUN bundle install
ONBUILD RUN rails db:migrate
ONBUILD RUN rails db:seed
