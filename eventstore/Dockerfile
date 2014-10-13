FROM ubuntu:14.04
MAINTAINER James Kelly <james@locationsolve.com>

RUN apt-get update && apt-get install -y curl

RUN curl http://download.geteventstore.com/binaries/EventStore-OSS-Linux-v3.0.0.tar.gz | tar xz -C /opt

EXPOSE 2113
EXPOSE 1113

VOLUME /data/db
VOLUME /data/logs

CMD cd /opt/EventStore-OSS-Linux-v3.0.0; ./run-node.sh --ext-tcp-port=1113 --int-tcp-port=1112 --ext-http-port=2113 --int-http-port=2112 --db /data/db --log /data/logs --int-ip=0.0.0.0 --ext-ip=0.0.0.0
