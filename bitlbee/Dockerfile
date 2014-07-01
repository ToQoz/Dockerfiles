FROM ubuntu:14.04

ENV DEBIAN_FRONTEND noninteractive

RUN apt-get -qy update
RUN apt-get -qy install bitlbee

RUN mkdir /var/run/bitlbee
RUN chown bitlbee:bitlbee /var/run/bitlbee

RUN mkdir -p /data/bitlbee/users
RUN chown -R bitlbee:bitlbee /data

EXPOSE 6667
WORKDIR /var/lib/bitlbee
VOLUME /data

ENTRYPOINT sudo -u bitlbee bitlbee -D -n -v -P /var/run/bitlbee/bitlbee.pid -d /data/bitlbee/users
