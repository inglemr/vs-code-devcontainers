FROM ruby:2.6.2-slim

RUN apt-get update -qy 
RUN apt-get install -y git-all gcc build-essential libpq-dev curl wget cmake pkg-config nodejs

RUN gem install bundler
COPY Gemfile Gemfile.lock ./
RUN bundle install
RUN echo 'alias rails="RAILS_ENV=development bundle exec rails"' >> ~/.bashrc
RUN echo 'alias rspec="RAILS_ENV=test bundle exec rspec"' >> ~/.bashrc
EXPOSE 3000
