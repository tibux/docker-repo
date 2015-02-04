FROM tibux/slackware-omnibus
MAINTAINER Thibaut Notteboom <thibaut.notteboom@gmail.com>

RUN cd /root && git clone https://github.com/chef/omnibus-chef
RUN cd /root/omnibus-chef && bundle install --without development

COPY libffi.rb /root/omnibus-chef/config/software/libffi.rb

RUN git config --global user.email "you@example.com" && git config --global user.name "Your Name"

ENV CHEF_VERSION 12.0.3
RUN echo "override :chef, version: \"${CHEF_VERSION}\"" >> /root/omnibus-chef/config/projects/chef.rb
RUN cd /root/omnibus-chef && bundle exec omnibus build chef -l debug

ENV CHEFDK_VERSION 0.4.0
RUN echo "override :chefdk, version: \"${CHEFDK_VERSION}\"" >> /root/omnibus-chef/config/projects/chefdk.rb
RUN cd /root/omnibus-chef && bundle exec omnibus build chefdk -l debug

# TODO
#RUN cd /root/omnibus-chef && bundle exec omnibus build push-jobs-client -l debug
