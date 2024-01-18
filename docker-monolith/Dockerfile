FROM ubuntu:18.04

RUN apt-get update
RUN apt-get install -y mongodb-server ruby-full ruby-dev bu...UN cd /reddit && rm Gemfile.lock && bundle install
RUN chmod 0777 /start.sh

CMD [\"/start.sh\"]