FROM centos:centos7
MAINTAINER Thibaut Notteboom <thibaut.notteboom@gmail.com>

RUN yum groupinstall -y 'Development Tools'
RUN yum install -y cmake ruby ruby-devel
RUN gem install --no-rdoc --no-ri bundler omnibus

RUN rpm -ivh http://download.fedoraproject.org/pub/epel/7/$(arch)/e/epel-release-7-5.noarch.rpm
RUN yum install -y fakeroot

# omnibus new <PROJECT>
# cd <PROJECT> && bundle install --path .bundle --binstubs
