FROM ruby:2.5.0

RUN apt-get update && apt-get install -y \
 	sqlite3

RUN gem install rails

ONBUILD ADD . /opt/app

ONBUILD WORKDIR /opt/app

ONBUILD RUN bundle install

ONBUILD RUN rails db:migrate

ONBUILD RUN rails db:seed
