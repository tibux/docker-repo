FROM tibux/slackware-omnibus
MAINTAINER Thibaut Notteboom <thibaut.notteboom@gmail.com>

#RUN cd /root && git clone https://github.com/chef/opscode-omnibus
RUN cd /root && git clone https://github.com/tibux/opscode-omnibus
RUN cd /root/opscode-omnibus && bundle install --binstubs

RUN echo "use_git_caching false" >> /root/opscode-omnibus/omnibus.rb

#COPY libffi.rb /root/opscode-omnibus/config/software/libffi.rb

#COPY erlang.rb /root/opscode-omnibus/config/software/erlang.rb
#RUN mkdir -p /root/opscode-omnibus/config/patches/erlang
#COPY fix-configure.patch /root/opscode-omnibus/config/patches/erlang/fix-configure.patch

#RUN sed -i "s;git@github.com:;https://github.com/;g" /root/opscode-omnibus/config/software/*

RUN cd /root/opscode-omnibus && bin/omnibus build chef-server -l debug
RUN cd /root/opscode-omnibus && bin/omnibus clean chef-server --purge

