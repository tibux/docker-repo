FROM vbatts/slackware:15.0
MAINTAINER Thibaut Notteboom <thibaut.notteboom@gmail.com>

RUN slackpkg -batch=on -default_answer=y update
RUN slackpkg -batch=on -default_answer=y upgrade patches || :

# gcc
RUN slackpkg -batch=on -default_answer=y install binutils gcc-11 gcc-g++-11 \
  gcc-go-11 glibc-2 libmpc kernel-headers make autoconf automake m4 zlib bc \
  guile gc libffi cmake libarchive nettle lzo libxml2 flex pkg-config pcre \
  doxygen libtool libcap bison

