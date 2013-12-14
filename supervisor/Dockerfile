FROM ubuntu:12.04
MAINTAINER How are you? "docker@howareyou.com"

RUN apt-get install -y python-setuptools
RUN easy_install supervisor
ADD ./supervisord.conf /etc/supervisord.conf

CMD /usr/local/bin/supervisord -c /etc/supervisord.conf
