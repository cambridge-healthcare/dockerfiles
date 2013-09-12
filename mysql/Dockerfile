FROM howareyou/precise
MAINTAINER How are you? "docker@howareyou.com"

ENV DEBIAN_FRONTEND noninteractive

RUN echo "mysql-server-5.5 mysql-server/start_on_boot boolean false" | debconf-set-selections

RUN chmod 777 /tmp

RUN apt-get -q install mysql-server-5.5

ADD mysql-listen.cnf /etc/mysql/conf.d/mysql-listen.cnf
ADD mysqld_start /mysqld_start
RUN chmod +x /mysqld_start

CMD /mysqld_start

EXPOSE 3306
