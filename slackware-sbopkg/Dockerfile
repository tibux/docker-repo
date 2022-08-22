FROM tibux/slackware-git:15.0
MAINTAINER Thibaut Notteboom <thibaut.notteboom@gmail.com>

# sbopkg
ENV TERM xterm

ARG sbopkg_version=0.38.2
ARG sbopkg_tag=1_wsr

RUN slackpkg -batch=on -default_answer=y install rsync

RUN wget https://github.com/sbopkg/sbopkg/releases/download/${sbopkg_version}/sbopkg-${sbopkg_version}-noarch-${sbopkg_tag}.tgz \
  && installpkg sbopkg-${sbopkg_version}-noarch-${sbopkg_tag}.tgz \
  && rm -f sbopkg-${sbopkg_version}-noarch-${sbopkg_tag}.tgz

RUN echo 'C' | sbopkg -r

