FROM tibux/slackware-omnibus
MAINTAINER Thibaut Notteboom <thibaut.notteboom@gmail.com>

RUN git config --global user.email "you@example.com" && git config --global user.name "Your Name"

ENV OHAI_VERSION 8.0.1
ENV CHEF_VERSION 12.0.3

RUN cd /root && git clone https://github.com/chef/omnibus-chef -b "chef-${CHEF_VERSION}"
RUN cd /root/omnibus-chef && bundle install --without development

COPY libffi.rb /root/omnibus-chef/config/software/libffi.rb
COPY chef.rb /root/omnibus-chef/config/software/chef.rb

RUN echo "build_version \"${CHEF_VERSION}\"" >> /root/omnibus-chef/config/projects/chef.rb
RUN echo "override :chef, version: \"${CHEF_VERSION}\"" >> /root/omnibus-chef/config/projects/chef.rb
RUN echo "override :ohai, version: \"${OHAI_VERSION}\"" >> /root/omnibus-chef/config/projects/chef.rb

RUN cd /root/omnibus-chef && bundle exec omnibus build chef -l debug
RUN cd /root/omnibus-chef && bundle clean chef --purge

