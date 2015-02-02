FROM tibux/slackware-sbopkg
MAINTAINER Thibaut Notteboom <thibaut.notteboom@gmail.com>

# jdk
ENV JDK_VERSION 8u31
RUN wget -O /var/cache/sbopkg/jdk-${JDK_VERSION}-linux-x64.tar.gz \
      --no-check-certificate -c --header "Cookie: oraclelicense=accept-securebackup-cookie" \
      http://download.oracle.com/otn-pub/java/jdk/${JDK_VERSION}-b13/jdk-${JDK_VERSION}-linux-x64.tar.gz
RUN sbopkg -Bi jdk && rm /var/run/sbopkg.pid

