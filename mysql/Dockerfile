FROM kaneshin/centos7:latest

MAINTAINER Shintaro Kaneko <kaneshin0120@gmail.com>

RUN yum -y install \
    wget \
    openssl-devel \
    libaio \
    net-tools


# Setup MySQL (5.6.21)
WORKDIR /tmp
RUN wget -q http://downloads.mysql.com/archives/get/file/MySQL-5.6.21-1.el7.x86_64.rpm-bundle.tar
RUN tar -xvf MySQL-5.6.21-1.el7.x86_64.rpm-bundle.tar
RUN rpm -Uh MySQL-client-5.6.21-1.el7.x86_64.rpm
RUN rpm -Uh MySQL-server-5.6.21-1.el7.x86_64.rpm 
WORKDIR /root
RUN service mysql start


# Define default command.
CMD ["/bin/bash"]

