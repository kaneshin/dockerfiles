FROM kaneshin/centos7:latest

MAINTAINER Shintaro Kaneko <kaneshin0120@gmail.com>

RUN yum -y install \
    git \
    mercurial


# Setup Go
RUN mkdir -p /root/goroot && curl https://storage.googleapis.com/golang/go1.3.3.linux-amd64.tar.gz | tar xvzf - -C /root/goroot --strip-components=1
RUN mkdir -p /root/gopath
ENV GOROOT /root/goroot
ENV GOPATH /root/gopath
ENV PATH $PATH:$GOROOT/bin:$GOPATH/bin
RUN echo 'export GOROOT=/root/goroot' >> /root/.bash_profile
RUN echo 'export GOPATH=/root/gopath' >> /root/.bash_profile
RUN echo 'export PATH=$PATH:$GOROOT/bin:$GOPATH/bin' >> /root/.bash_profile


# Define default command.
CMD ["/bin/bash"]

