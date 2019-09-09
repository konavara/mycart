# This is docker file for mycart MS Frontend Layer
# First uncommented line follows
FROM centos:7
MAINTAINER konavara@gmail.com
RUN yum -y update
RUN yum -y install httpd php php-gd php-mysql
ADD config /opt
RUN yum -y install `cat /opt/packages`
RUN yum -y install `cat /opt/myapppackages`
ADD code /var/www/html
EXPOSE 80
ENV BACKENDLB=test
ENV MY_DB_HOST_WRITE=test;
ENV MY_DB_NAME=test
ENV MY_DB_USER=test;
ENV MY_DB_PASS=test;
ADD scripts /usr/bin
RUN chmod 755 /usr/bin/startapache
CMD ["startapache"]