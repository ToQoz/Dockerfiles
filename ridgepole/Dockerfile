FROM alpine:3.3

# https://pkgs.alpinelinux.org/package/v3.3/main/x86/ruby-mysql2
# https://pkgs.alpinelinux.org/package/v3.4/main/x86/ruby-mysql2 ---> 404

RUN apk update && apk upgrade && \
  apk --update add --virtual build-dependencies build-base ruby-dev && \
  apk --update add openssl ca-certificates postgresql-dev ruby ruby-json ruby-bigdecimal ruby-mysql2 && \
  gem install pg --no-ri --no-rdoc -- --with-pg-lib=/usr/lib && \
  gem install activerecord-mysql-awesome --no-ri --no-rdoc && \
  gem install ridgepole -v 0.7.1 --no-ri --no-rdoc && \
  gem cleanup && \
  apk del build-dependencies && \
  rm -rf /var/cache/apk/*

ENTRYPOINT ["ridgepole"]
