FROM tibux/slackware-multilib:15.0
MAINTAINER Thibaut Notteboom <thibaut.notteboom@gmail.com>

RUN slackpkg -batch=on -default_answer=y install atk cairo fontconfig freetype fribidi glib2 graphite2 gdk-pixbuf2 gettext-tools gtk+3 harfbuzz itstool libepoxy libglvnd libnotify libpng libtiff libxcb libxkbcommon libICE libSM libXau libXaw libXcomposite libXcursor libXdamage libXdmcp libXext libXfixes libXft libXi libXinerama libXmu libXrandr libXrender libXpm libXt libX11 meson ninja pango pixman python3 shared-mime-info wayland xorgproto xterm
RUN sbopkg -Bi "zenity steam" -e stop
