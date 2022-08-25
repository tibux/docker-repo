FROM tibux/slackware-multilib:15.0
MAINTAINER Thibaut Notteboom <thibaut.notteboom@gmail.com>

RUN slackpkg -batch=on -default_answer=y install fontconfig freetype fribidi glib2 graphite2 gtk+3 harfbuzz libpng libXrender meson pango python3 xorgproto
RUN sbopkg -Bi "zenity steam"
