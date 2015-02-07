FROM tibux/slackware-omnibus
MAINTAINER Thibaut Notteboom <thibaut.notteboom@gmail.com>

RUN git config --global user.email "you@example.com" && git config --global user.name "Your Name"

RUN cd /root && git clone https://github.com/chef/opscode-omnibus

RUN cd /root/opscode-omnibus && bundle install --binstubs

COPY libffi.rb /root/opscode-omnibus/config/software/libffi.rb

COPY erlang.rb /root/opscode-omnibus/config/software/erlang.rb
RUN mkdir -p /root/opscode-omnibus/config/patches/erlang
COPY fix-configure.patch /root/opscode-omnibus/config/patches/erlang/fix-configure.patch

RUN sed -i "s;git@github.com:;https://github.com/;g" /root/opscode-omnibus/config/software/*

RUN cd /root/opscode-omnibus && bin/omnibus build chef-server -l debug
RUN cd /root/opscode-omnibus && bin/omnibus clean chef-server --purge

