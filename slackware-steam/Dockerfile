FROM tibux/slackware-multilib:15.0
MAINTAINER Thibaut Notteboom <thibaut.notteboom@gmail.com>

RUN slackpkg -batch=on -default_answer=y install freetype glib2 gtk+3 harfbuzz libpng meson pango python3
RUN sbopkg -Bi "zenity steam"
