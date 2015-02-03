FROM tibux/slackware-omnibus
MAINTAINER Thibaut Notteboom <thibaut.notteboom@gmail.com>

RUN cd /root && git clone https://github.com/chef/omnibus-chef
RUN cd /root/omnibus-chef && bundle install --without development

COPY libffi.rb /root/omnibus-chef/config/software/libffi.rb

RUN git config --global user.email "you@example.com" && git config --global user.name "Your Name"
RUN bundle exec omnibus build chef -l debug
RUN bundle exec omnibus build chef-dk -l debug
RUN bundle exec omnibus build chef-container -l debug
