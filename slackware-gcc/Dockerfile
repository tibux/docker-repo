FROM vbatts/slackware:14.2
MAINTAINER Thibaut Notteboom <thibaut.notteboom@gmail.com>

RUN slackpkg -batch=on -default_answer=y update
RUN slackpkg -batch=on -default_answer=y upgrade patches

# gcc
RUN slackpkg -batch=on -default_answer=y install binutils gcc-5 gcc-g++-5 \
  glibc-2 libmpc kernel-headers make autoconf automake m4 zlib bc \
  cmake libarchive nettle lzo libxml2

