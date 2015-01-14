FROM vbatts/slackware
MAINTAINER Thibaut Notteboom <thibaut.notteboom@gmail.com>

RUN slackpkg update

# gcc
RUN slackpkg -batch=on -default_answer=y install binutils gcc-4 gcc-g++-4 glibc-2 libmpc kernel-headers make
RUN slackpkg -batch=on -default_answer=y install autoconf automake m4 zlib

# git
RUN slackpkg -batch=on -default_answer=y install git-1 curl cyrus-sasl-2.1
RUN git config --global user.email "you@example.com" && git config --global user.name "Your Name"

# omnibus
RUN slackpkg -batch=on -default_answer=y install libyaml ruby perl
RUN gem install --no-ri --no-rdoc omnibus bundle

