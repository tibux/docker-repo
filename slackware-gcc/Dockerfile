FROM vbatts/slackware
MAINTAINER Thibaut Notteboom <thibaut.notteboom@gmail.com>

RUN slackpkg update

# gcc
RUN slackpkg -batch=on -default_answer=y install binutils gcc-4 gcc-g++-4 glibc-2 libmpc kernel-headers make autoconf automake m4 zlib

