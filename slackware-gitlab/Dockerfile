FROM tibux/slackware-omnibus
MAINTAINER Thibaut Notteboom <thibaut.notteboom@gmail.com>

ENV GITLAB_VERSION 7-11-stable

RUN slackpkg -batch=on -default_answer=y install bison flex

RUN cd /root && git clone https://gitlab.com/gitlab-org/omnibus-gitlab.git
RUN cd /root/omnibus-gitlab && git checkout ${GITLAB_VERSION}
RUN cd /root/omnibus-gitlab && bundle install --path .bundle --binstubs

RUN echo "use_git_caching false" >> /root/omnibus-gitlab/omnibus.rb

COPY libffi.rb /root/omnibus-gitlab/config/software/libffi.rb

RUN cd /root/omnibus-gitlab && bin/omnibus build gitlab

RUN sh /root/omnibus-gitlab/pkg/gitlab-*.x86_64.sh

