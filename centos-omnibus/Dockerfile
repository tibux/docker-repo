FROM centos:centos7
MAINTAINER Thibaut Notteboom <thibaut.notteboom@gmail.com>

RUN yum groupinstall -y 'Development Tools'
RUN yum install -y cmake ruby ruby-devel
RUN gem install bundler

RUN adduser -c 'Omnibus Build' omnibus-build
RUN install -d /var/cache/omnibus -o omnibus-build -g omnibus-build

RUN rpm -ivh http://download.fedoraproject.org/pub/epel/7/$(arch)/e/epel-release-7-5.noarch.rpm
RUN yum install -y fakeroot

# bundle install --path .bundle --binstubs
