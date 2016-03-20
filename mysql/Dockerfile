FROM mysql:5.7.11

ENV DEBIAN_FRONTEND noninteractive
ENV LC_ALL C

RUN apt-get -y update && \
  apt-get install -y --no-install-recommends mecab mecab-ipadic-utf8 && \
  apt-get clean && rm -fr /var/lib/apt/lists/* /tmp/* /var/tmp/*

ADD conf.d/mecab.cnf /etc/mysql/conf.d/mecab.cnf
