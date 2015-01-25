FROM tibux/slackware-gcc
MAINTAINER Thibaut Notteboom <thibaut.notteboom@gmail.com>

# sbopkg
ENV TERM xterm
RUN slackpkg -batch=on -default_answer=y install cyrus-sasl-2.1 rsync
RUN wget http://sbopkg.googlecode.com/files/sbopkg-0.37.0-noarch-1_cng.tgz && installpkg sbopkg-0.37.0-noarch-1_cng.tgz && rm -f sbopkg-0.37.0-noarch-1_cng.tgz
RUN mkdir -p /var/lib/sbopkg/SBo/`cat /etc/slackware-version |awk -F' ' '{print $2}'` /var/lib/sbopkg/queues /var/log/sbopkg /var/cache/sbopkg /tmp/SBo
RUN sbopkg -r && rm /var/run/sbopkg.pid

