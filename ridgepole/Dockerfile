FROM alpine:3.3

# https://pkgs.alpinelinux.org/package/v3.3/main/x86/ruby-mysql2
# https://pkgs.alpinelinux.org/package/v3.4/main/x86/ruby-mysql2 ---> 404

RUN apk update && apk upgrade && \
  apk --update add openssl ca-certificates ruby ruby-json ruby-bigdecimal ruby-mysql2 && \
  gem install activerecord-mysql-awesome ridgepole --no-ri --no-rdoc && \
  gem cleanup && \
  rm -rf /var/cache/apk/*

ENTRYPOINT ["ridgepole"]
