FROM tibux/slackware-git
MAINTAINER Thibaut Notteboom <thibaut.notteboom@gmail.com>

# sbopkg
ENV TERM xterm

RUN slackpkg -batch=on -default_answer=y install rsync

RUN wget https://github.com/sbopkg/sbopkg/releases/download/0.38.1/sbopkg-0.38.1-noarch-1_wsr.tgz && \
    installpkg sbopkg-0.38.1-noarch-1_cng.tgz && rm -f sbopkg-0.38.1-noarch-1_cng.tgz

RUN mkdir -p /var/lib/sbopkg/SBo/`cat /etc/slackware-version \
    | awk -F' ' '{print $2}'` /var/lib/sbopkg/queues /var/log/sbopkg /var/cache/sbopkg /tmp/SBo

RUN sbopkg -r && rm /var/run/sbopkg.pid

