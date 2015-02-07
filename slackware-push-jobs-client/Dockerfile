FROM tibux/slackware-omnibus
MAINTAINER Thibaut Notteboom <thibaut.notteboom@gmail.com>

RUN git config --global user.email "you@example.com" && git config --global user.name "Your Name"

RUN cd /root && git clone https://github.com/chef/omnibus-chef
RUN cd /root/omnibus-chef && bundle install --without development

RUN cd /root/omnibus-chef && bundle exec omnibus build push-jobs-client
RUN cd /root/omnibus-chef && bundle exec omnibus clean push-jobs-client --purge

