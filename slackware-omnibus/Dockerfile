FROM tibux/slackware-gcc
MAINTAINER Thibaut Notteboom <thibaut.notteboom@gmail.com>

# git
RUN slackpkg -batch=on -default_answer=y install git-1 curl cyrus-sasl-2.1

# omnibus
RUN slackpkg -batch=on -default_answer=y install libyaml ruby perl
RUN gem install --no-ri --no-rdoc omnibus bundle

