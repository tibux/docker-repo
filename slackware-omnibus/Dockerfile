FROM tibux/slackware-git
MAINTAINER Thibaut Notteboom <thibaut.notteboom@gmail.com>

# omnibus
RUN slackpkg -batch=on -default_answer=y install libyaml ruby perl
RUN gem install --no-ri --no-rdoc omnibus bundle

