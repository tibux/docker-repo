FROM tibux/slackware-sbopkg
MAINTAINER Thibaut Notteboom <thibaut.notteboom@gmail.com>

# jdk
RUN wget -O /var/cache/sbopkg/jdk-7u71-linux-x64.tar.gz \
      --no-check-certificate -c --header "Cookie: oraclelicense=accept-securebackup-cookie" \
      http://download.oracle.com/otn-pub/java/jdk/7u71-b14/jdk-7u71-linux-x64.tar.gz
RUN sbopkg -Bi jdk && rm /var/run/sbopkg.pid

