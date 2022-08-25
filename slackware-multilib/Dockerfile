FROM tibux/slackware-sbopkg:15.0
MAINTAINER Thibaut Notteboom <thibaut.notteboom@gmail.com>

RUN slackpkg -batch=on -default_answer=y install lftp

RUN lftp -c 'open http://bear.alienbase.nl/mirrors/people/alien/multilib/ ; mirror -c -e 15.0'

RUN upgradepkg --reinstall --install-new ./15.0/*.t?z
RUN upgradepkg --install-new ./15.0/slackware64-compat32/*-compat32/*.t?z

RUN chmod +x /etc/profile.d/32dev.sh

RUN echo '\
        . /etc/profile ; \
    ' >> /root/.profile
