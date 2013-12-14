FROM howareyou/ubuntu:12.04
# MAINTAINER How are you? "docker@howareyou.com"

RUN \
  . /.profile ;\
  echo "mysql-server-5.5 mysql-server/start_on_boot boolean false" | debconf-set-selections ;\
  chmod 777 /tmp ;\
  apt-get install mysql-server-5.5 ;\
# END RUN

ADD mysql-listen.cnf /etc/mysql/conf.d/mysql-listen.cnf
ADD mysqld_start /mysqld_start
RUN chmod +x /mysqld_start

CMD /mysqld_start

EXPOSE 3306
