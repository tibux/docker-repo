FROM tibux/slackware-multilib:15.0
MAINTAINER Thibaut Notteboom <thibaut.notteboom@gmail.com>

RUN slackpkg -batch=on -default_answer=y install atk cairo fontconfig freetype fribidi glib2 graphite2 gdk-pixbuf2 gettext-tools gtk+3 harfbuzz itstool libnotify libpng libxcb libXau libXdmcp libXaw libXext libXft libXinerama libXmu libXrender libXpm libX11 meson ninja pango pixman python3 shared-mime-info xorgproto xterm
RUN sbopkg -Bi "zenity steam"
