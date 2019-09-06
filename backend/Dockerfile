# This is docker file for mycart MS Frontend Layer
# First uncommented line follows
FROM centos:7
MAINTAINER konavara@gmail.com
RUN yum -y update
ADD config /opt
RUN yum -y install `cat /opt/packages`
RUN yum -y install `cat /opt/myapppackages`
ADD code /var/www/html
EXPOSE 80
ENV BACKENDLB=test
ADD scripts /usr/bin
RUN chmod 755 /usr/bin/startapache
CMD ["startapache"]