FROM ruby:2.0.0

ONBUILD WORKDIR /opt

ONBUILD COPY app .

ONBUILD RUN apt-get update; \
	apt-get install -y sqlite3 libsqlite3-dev nodejs;

ONBUILD WORKDIR /opt/app

ONBUILD RUN	bundle install --without production; \
	rake db:create; \
	rake db:migrate;
