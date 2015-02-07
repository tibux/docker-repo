FROM tibux/slackware-omnibus
MAINTAINER Thibaut Notteboom <thibaut.notteboom@gmail.com>

RUN git config --global user.email "you@example.com" && git config --global user.name "Your Name"

ENV OHAI_VERSION 7.4.1

RUN cd /root && git clone https://github.com/chef/omnibus-chef
RUN cd /root/omnibus-chef && bundle install --without development

RUN echo "override :ohai, version: \"${OHAI_VERSION}\"" >> /root/omnibus-chef/config/projects/push-jobs-client.rb

COPY libffi.rb /root/omnibus-chef/config/software/libffi.rb

RUN cd /root/omnibus-chef && bundle exec omnibus build push-jobs-client
RUN cd /root/omnibus-chef && bundle exec omnibus clean push-jobs-client --purge

