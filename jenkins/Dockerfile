FROM howareyou/precise
MAINTAINER How are you? "docker@howareyou.com"

RUN apt-get install openjdk-7-jre-headless
ADD http://mirrors.jenkins-ci.org/war-stable/latest/jenkins.war /usr/local/bin/jenkins.war

ADD github /github
RUN chmod +x /github
RUN /github

CMD java -jar /usr/local/bin/jenkins.war
