FROM tibux/slackware-sbopkg
MAINTAINER Thibaut Notteboom <thibaut.notteboom@gmail.com>

RUN slackpkg -batch=on -default_answer=y install lftp

RUN lftp -c 'open http://bear.alienbase.nl/mirrors/people/alien/multilib/ ; mirror -c -e 14.2'

RUN upgradepkg --reinstall --install-new ./14.2/*.t?z
RUN upgradepkg --install-new ./14.2/slackware64-compat32/*-compat32/*.t?z

RUN . /etc/profile.d/32dev.sh

RUN sbopkg -Bi OpenAL -Bi steam
