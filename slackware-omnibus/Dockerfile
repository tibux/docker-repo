FROM tibux/slackware-git:15.0
MAINTAINER Thibaut Notteboom <thibaut.notteboom@gmail.com>

# omnibus
RUN slackpkg -batch=on -default_answer=y install libyaml ruby gmp gc guile libffi libunistring
RUN gem install --no-document omnibus bundle

