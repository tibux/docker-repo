FROM tibux/slackware-sbopkg
MAINTAINER Thibaut Notteboom <thibaut.notteboom@gmail.com>

RUN sbopkg -Bi amazon-corretto

ENV JAVA_HOME /usr/lib64/java
ENV PATH ${PATH}:${JAVA_HOME}/bin:${JAVA_HOME}/jre/bin
