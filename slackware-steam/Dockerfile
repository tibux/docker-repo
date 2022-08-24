FROM tibux/slackware-multilib:15.0
MAINTAINER Thibaut Notteboom <thibaut.notteboom@gmail.com>

RUN slackpkg -batch=on -default_answer=y install pango gtk+3 meson python3
RUN sbopkg -Bi "zenity steam"
