FROM tibux/slackware-omnibus:15.0
MAINTAINER Thibaut Notteboom <thibaut.notteboom@gmail.com>

#ENV OHAI_VERSION 8.3.0
#ENV CHEF_VERSION 12.4.1

RUN slackpkg -batch=on -default_answer=y install flex

RUN cd /root && git clone https://github.com/chef/chef
RUN cd /root/chef/omnibus && bundle install --without development

RUN echo "use_git_caching false" >> /root/chef/omnibus/omnibus.rb

RUN cd /root/chef/omnibus && bundle exec omnibus build chef
RUN cd /root/chef/omnibus && bundle exec omnibus clean chef --purge

RUN sh /root/chef/omnibus/pkg/chef-*.x86_64.sh

