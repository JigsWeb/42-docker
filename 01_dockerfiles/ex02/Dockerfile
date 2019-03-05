FROM ruby:2.0.0

EXPOSE 3000/tcp

WORKDIR /opt

COPY app .

RUN apt-get update; \
	apt-get install -y sqlite3 libsqlite3-dev nodejs;

WORKDIR app

RUN	bundle install --without production; \
	rake db:create; \
	rake db:migrate; 

CMD ["rails", "s", "-b", "0.0.0.0", "-p" ,"3000"]
