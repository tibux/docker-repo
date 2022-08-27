FROM tibux/slackware-multilib:15.0
MAINTAINER Thibaut Notteboom <thibaut.notteboom@gmail.com>

RUN slackpkg -batch=on -default_answer=y install cairo fontconfig freetype fribidi glib2 graphite2 gtk+3 harfbuzz libpng libxcb libXau libXdmcp libXft libXrender libX11 meson pango pixman python3 xorgproto
RUN sbopkg -Bi "zenity steam"
