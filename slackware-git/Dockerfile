FROM tibux/slackware-gcc
MAINTAINER Thibaut Notteboom <thibaut.notteboom@gmail.com>

# git
RUN slackpkg -batch=on -default_answer=y install git-1 curl cyrus-sasl-2.1 ca-certificates perl
RUN /usr/bin/c_rehash

