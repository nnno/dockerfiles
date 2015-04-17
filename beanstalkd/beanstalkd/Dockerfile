FROM ubuntu:14.04
MAINTAINER Yusuke Unno <nnno@nnno.jp>

ENV DEBIAN_FRONTEND noninteractive

RUN apt-get update && apt-get install -y beanstalkd
RUN apt-get clean && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*

EXPOSE 11300
VOLUME ["/data"]
CMD ["/usr/bin/beanstalkd", "-f", "60000", "-b", "/data"]


