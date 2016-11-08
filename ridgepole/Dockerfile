FROM alpine:3.3

RUN apk add --no-cache --update ruby ruby-json ruby-mysql2 ruby-bigdecimal mysql-client && \
  rm -rf /var/cache/apk/* && \
  gem install --no-ri --no-rdoc activerecord-mysql-awesome ridgepole
