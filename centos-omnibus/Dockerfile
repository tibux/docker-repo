FROM centos:centos7
MAINTAINER Thibaut Notteboom <thibaut.notteboom@gmail.com>

RUN yum groupinstall -y 'Development Tools'
RUN yum install -y cmake ruby ruby-devel
#RUN gem install --no-rdoc --no-ri bundler omnibus

RUN yum install -y epel-release fakeroot

# omnibus new <PROJECT>
# cd <PROJECT> && bundle install --path .bundle --binstubs
