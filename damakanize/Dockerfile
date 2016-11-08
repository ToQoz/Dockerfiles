FROM alpine:3.4

RUN apk --update add openssl ca-certificates ruby && \
  gem install amakanize --no-ri --no-rdoc && \
  gem cleanup && \
  rm -rf /var/cache/apk/*

ADD damakanize /usr/local/bin/damakanize
ENTRYPOINT ["damakanize"]
