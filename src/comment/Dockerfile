FROM ruby:2.2
RUN set -x \
&& echo "deb http://archive.debian.org/debian stretch main" > /etc/apt/sources.list \
&& apt-get update -qq && apt-get install -y build-essential \
&& apt-get clean

ENV APP_HOME /app
RUN mkdir $APP_HOME
WORKDIR $APP_HOME

ADD Gemfile* $APP_HOME/
RUN bundle install
ADD . $APP_HOME

ENV COMMENT_DATABASE_HOST comment_db
ENV COMMENT_DATABASE comments

CMD ["puma"]
