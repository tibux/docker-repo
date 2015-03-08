FROM tibux/slackware-omnibus
MAINTAINER Thibaut Notteboom <thibaut.notteboom@gmail.com>

ENV OHAI_VERSION 8.0.1
ENV CHEF_VERSION 12.0.3

RUN cd /root && git clone https://github.com/chef/omnibus-chef -b "chef-${CHEF_VERSION}"
RUN cd /root/omnibus-chef && bundle install --without development

RUN echo "use_git_caching false" >> /root/omnibus-chef/omnibus.rb

COPY libffi.rb /root/omnibus-chef/config/software/libffi.rb
COPY chef.rb /root/omnibus-chef/config/projects/chef.rb

RUN echo "build_version \"${CHEF_VERSION}\"" >> /root/omnibus-chef/config/projects/chef.rb
RUN echo "override :chef, version: \"${CHEF_VERSION}\"" >> /root/omnibus-chef/config/projects/chef.rb
RUN echo "override :ohai, version: \"${OHAI_VERSION}\"" >> /root/omnibus-chef/config/projects/chef.rb

RUN cd /root/omnibus-chef && bundle exec omnibus build chef
RUN cd /root/omnibus-chef && bundle exec omnibus clean chef --purge

RUN sh /root/omnibus-chef/pkg/chef-${CHEF_VERSION}_1.x86_64.sh

