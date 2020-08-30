FROM ruby:2.6.5-alpine

# Update installation source for alpinelinux
RUN sed -i 's/dl-cdn.alpinelinux.org/mirrors.aliyun.com/g' /etc/apk/repositories
# Install the dependencies
RUN apk update && apk add bash
RUN apk --update add build-base patch vim imagemagick tzdata nodejs yarn libxslt-dev yaml-dev sqlite-dev libxml2-dev 
#We use the command RUN on the Dockerfile to execute the commands we want to use in the image.

ENV APP_HOME /app
RUN mkdir $APP_HOME
WORKDIR $APP_HOME

# Add a script to be executed every time the container starts.
COPY docker/entrypoint.sh /usr/bin/
RUN chmod +x /usr/bin/entrypoint.sh
ENTRYPOINT ["entrypoint.sh"]

RUN gem install bundler:2.1.4
ADD Gemfile* $APP_HOME/
RUN bundle lock --add-platform x86-mingw32 x86-mswin32 x64-mingw32 java
RUN bundle install

ADD . $APP_HOME
RUN yarn install --check-files

# start app
CMD ["rm", "$APP_HOME/tmp/pids/server.pid"]
CMD ["rails","server","-b","0.0.0.0"]
