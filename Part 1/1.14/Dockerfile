FROM ruby:2.6.0

COPY . .

RUN apt-get update

RUN apt-get install -y --allow-unauthenticated nodejs

RUN gem install bundler

RUN bundle install 

RUN rails db:migrate

EXPOSE 3000

CMD ["rails", "s"]
