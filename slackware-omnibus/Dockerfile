FROM tibux/slackware-git
MAINTAINER Thibaut Notteboom <thibaut.notteboom@gmail.com>

# omnibus
#RUN slackpkg -batch=on -default_answer=y install libyaml ruby perl
RUN slackpkg -batch=on -default_answer=y install libyaml readline gdbm lftp

RUN lftp -c "mirror -c http://ftp.slackware.com/pub/slackware/slackware64-current/source/d/ruby/ /tmp/ruby"
RUN cd /tmp/ruby && sh ruby.SlackBuild
RUN installpkg /tmp/ruby-*.txz && rm /tmp/ruby-*.txz
RUN removepkg readline gdbm

RUN gem install --no-ri --no-rdoc omnibus bundle

