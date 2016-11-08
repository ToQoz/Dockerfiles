FROM alpine:3.4

RUN apk --update add ruby ruby-json ruby-mysql2 ruby-bigdecimal mysql-client && \
  gem install activerecord-mysql-awesome ridgepole --no-ri --no-rdoc \
  gem cleanup && \
  rm -rf /var/cache/apk/*

ENTRYPOINT ["ridgepole"]
